# jsMind + Vue 3

This is a sample of how to use jsmind in your vue project.

## Install jsMind

jsmind@0.7.1 or later versions is required

```bash
npm install jsmind
```

## Create component

Create a new component and add to `App`

```vue
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
                    // ...
                }
            }
        },
        mounted() {
            let options = Object.assign(this.jsmind_options, {
                container: this.$refs.jsmind_container
            });
            let jm = new jsMind(options);
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
    <div ref="jsmind_container" class="jsmind-container"></div>
</template>
```

## Build your project

```bash
npm run build
```

## More

jsMind project home: <a href="https://github.com/hizzgdev/jsmind">https://github.com/hizzgdev/jsmind</a>
