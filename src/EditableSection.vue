<template>
    <div class="quill-editor">
        <div class="ql-editor" v-html="formattedValue" v-if="!edit" @dblclick="edit = true"></div>
        <div v-else>
            <quill-editor :value="value" @change="onEditorChange($event)">
            </quill-editor>
            <button @click="close">Bekreft</button>
        </div>
    </div>
</template>

<script>
    // require styles
    import 'quill/dist/quill.core.css'
    import 'quill/dist/quill.snow.css'
    import 'quill/dist/quill.bubble.css'

    import {quillEditor} from 'vue-quill-editor';

    export default {
        components: {
            quillEditor
        },
        props: {
            value: String,
            variables: Object
        },

        data() {
            return {
                edit: false,
                editedContent: null
            }
        },

        methods: {
            onEditorChange(evt) {
                console.log(evt);
                this.editedContent = evt.html;
            },

            close() {
                this.edit = false;
                if (this.editedContent) {
                    this.$emit('input', this.editedContent)
                }
            }
        },

        computed: {
            formattedValue() {
                let value = this.value;
                Object.keys(this.variables).forEach(variable => {
                    value = value.replace(`{{${variable}}}`, this.variables[variable]);
                });
                return value;
            }
        }
    }
</script>