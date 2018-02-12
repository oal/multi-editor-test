<template>
    <div class="tui-container">
        <editable-section :value="part" @input="onInput($event, index)" v-for="(part, index) in content"
                        :variables="variables"
                        :key="index">
        </editable-section>
    </div>
</template>

<script>
    // import TuiViewer from './TuiViewer.vue';
    import EditableSection from './EditableSection.vue';

    export default {
        components: {
            EditableSection
        },

        props: {
            value: String,
            variables: Object
        },

        methods: {
            onInput(value, index) {
                console.log(value);
                let content = [...this.content].filter(v => !!v);
                content[index] = value;
                this.content = content;
            }
        },

        computed: {
            content: {
                get() {
                    return this.value.split('<br>');
                },
                set(val) {
                    this.$emit('input', val.join('<br>'));
                }
            }
        }
    }
</script>

<style scoped>
</style>