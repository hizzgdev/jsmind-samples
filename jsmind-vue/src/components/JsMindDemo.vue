<script>
    import jsMind from 'jsmind'
    import 'jsmind/draggable-node'
    import 'jsmind/style/jsmind.css'

    export default {
        data() {
            return {
                jsmind_options : {
                    editable: true,
                    theme: 'primary',
                },
                jsmind_data : {
                    meta: {
                        name: 'jsMind sample',
                        author: 'hizzgdev@163.com',
                        version: '0.7.1',
                    },
                    format: 'node_tree',
                    data: {
                        id: 'root',
                        topic: 'jsMind',
                        children: [
                            {
                                id: 'easy',
                                topic: 'Easy',
                                direction: 'left',
                                children: [
                                    { id: 'easy1', topic: 'Easy to show' },
                                    { id: 'easy2', topic: 'Easy to edit' },
                                    { id: 'easy3', topic: 'Easy to store' },
                                    { id: 'easy4', topic: 'Easy to embed' },
                                    {
                                        'id': 'other3',
                                        'background-image': 'https://hizzgdev.github.io/jsmind/example/ant.png',
                                        'width': '100',
                                        'height': '100',
                                    },
                                ],
                            },
                            {
                                id: 'open',
                                topic: 'Open Source',
                                direction: 'right',
                                children: [
                                    {
                                        'id': 'open1',
                                        'topic': '<a href="https://github.com/hizzgdev/jsmind" target="_blank">on GitHub</a>',
                                        'background-color': '#eee',
                                        'foreground-color': 'blue',
                                    },
                                    { id: 'open2', topic: 'BSD License' },
                                ],
                            },
                            {
                                id: 'powerful',
                                topic: 'Powerful',
                                direction: 'right',
                                children: [
                                    { id: 'powerful1', topic: 'Base on Javascript' },
                                    { id: 'powerful2', topic: 'Base on HTML5' },
                                    { id: 'powerful3', topic: 'Depends on you' },
                                ],
                            },
                            {
                                id: 'other',
                                topic: 'test node',
                                direction: 'left',
                                children: [ ],
                            },
                        ],
                    },
                }
            }
        },
        mounted() {
            let options = this.jsmind_options;
            options.container = this.$refs.jsmind_container;
            let jm = new jsMind(this.jsmind_options);
            jm.show(this.jsmind_data);
        }

    }
</script>

<style scoped>
    .jsmind-container {
        width: 1024px;
        height: 700px;
        border: solid 1px #ccc;
    }
</style>

<template>
    <p>For detailed documentation, see the project homepage: <a href="https://github.com/hizzgdev/jsmind">https://github.com/hizzgdev/jsmind</a></p>
    <div ref="jsmind_container" class="jsmind-container"></div>
</template>