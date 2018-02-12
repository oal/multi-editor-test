<template>
    <div id="app">
        <multi-editor v-model="content" :variables="variables"></multi-editor>
    </div>
</template>

<script>
    import MultiEditor from './MultiEditor.vue';

    export default {
        components: {
            MultiEditor
        },
        name: 'app',
        data() {
            return {
                variables: {
                    name: 'test name'
                },
                content: `<h2 class="ql-align-justify">Lorem ipsum dolor sit amet, consectetur adipiscing elit. {{name}} Praesent eu dui non arcu vulputate lobortis. </h2><p class="ql-align-justify"><br></p><p class="ql-align-justify">Quisque lacinia mauris at ligula fringilla, ac sollicitudin ante efficitur. In tempor, turpis at imperdiet consectetur, ipsum odio condimentum risus, et dapibus felis ante nec lectus. Ut euismod tellus vel orci pretium convallis. Nulla facilisi. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Fusce turpis augue, faucibus quis mollis vitae, congue sit amet nisl.</p><p class="ql-align-justify"><br></p><p class="ql-align-justify">Mauris a auctor erat,</p><h1 class="ql-align-justify">. vel vestibulum massa. Nunc dictum magna tellus, id fermentum nisl faucibus a. Nunc elementum eros non purus ultrices, nec placerat ipsum suscipit. In hac habitasse platea dictumst. Maecenas eget posuere enim. Etiam libero augue, placerat nec nunc in, mattis auctor erat. Nunc at magna ullamcorper, imperdiet lorem non, pellentesque lorem. Aenean nec tristique risus. Donec ultricies leo erat, vitae porttitor nisl maximus id.</h1><p class="ql-align-justify"><br></p><p class="ql-align-justify">In sollicitudin est et enim aliquet mollis. Ut quis metus lorem. Cras a turpis id libero lacinia fringilla in et mauris. Quisque finibus metus odio, a imperdiet nulla iaculis quis. Donec nisl justo, molestie non diam at, aliquam pretium risus. Morbi ac porttitor purus, vel gravida neque. Ut hendrerit augue sapien, finibus placerat nibh sodales eget. Etiam feugiat dolor in neque auctor ultrices. Donec viverra erat eu magna maximus gravida. Mauris commodo est vitae lorem finibus fermentum ut viverra mi. Pellentesque blandit, elit in luctus vulputate, est lorem suscipit sem, venenatis volutpat risus libero non leo. Etiam maximus nibh eu laoreet faucibus. Cras tristique odio at porttitor suscipit.</p><p class="ql-align-justify"><br></p><p class="ql-align-justify">Phasellus vel neque vitae nisi pharetra consequat. Nulla eget neque arcu. In ut mollis orci, vulputate facilisis metus. Maecenas ullamcorper velit odio, nec gravida erat pharetra eget. Vivamus semper congue efficitur. Mauris iaculis mauris eu erat finibus, sed eleifend libero lobortis. Donec tempor mauris scelerisque odio tristique cursus. Nulla enim enim, consequat at arcu a, finibus pretium sapien. Nunc placerat, lacus ut sollicitudin venenatis, ipsum nisl commodo velit, a egestas velit felis a turpis. Mauris at tortor dui. Ut rutrum sapien a nibh lobortis, sit amet aliquet urna faucibus. Phasellus nulla est, venenatis et rhoncus at, gravida sit amet lorem. Morbi id lobortis metus. Cras ac elit nulla. Curabitur blandit sollicitudin massa, nec pulvinar urna malesuada eu.</p><p class="ql-align-justify"><br></p><p class="ql-align-justify">Proin rutrum consectetur tincidunt. Sed eleifend volutpat justo eu aliquet. Nulla vehicula volutpat enim et ullamcorper. Ut rutrum odio ac lorem aliquam, a pellentesque elit porttitor. Aenean sed ipsum porttitor, vestibulum est sit amet, ultrices nunc. Vestibulum accumsan mi et porta aliquam. Curabitur sollicitudin massa in placerat vehicula. Praesent a nunc sit amet mauris accumsan blandit. Phasellus malesuada in arcu id consequat. Etiam cursus congue lobortis. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin sem neque, commodo et hendrerit sit amet, fermentum eu urna. Quisque at dolor nec ipsum pretium rutrum id et tortor. Maecenas malesuada nunc nec leo congue vehicula.</p><p class="ql-align-justify"><br></p><p><br></p>`
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        color: #2c3e50;
    }
</style>
