# jsMind in HTML

This is a sample of how to use jsmind in a simple HTML file.

## Install jsMind

Option 1: use CDN jsDeliver [[sample](./jsmind-jsdelivr.html)]

```html
<link type="text/css" rel="stylesheet" href="//cdn.jsdelivr.net/npm/jsmind@0.8.1/style/jsmind.css"/>

<script src="//cdn.jsdelivr.net/npm/jsmind@0.8.1/es6/jsmind.js"></script>
<script src="//cdn.jsdelivr.net/npm/jsmind@0.8.1/es6/jsmind.draggable-node.js"></script>
```

Option 2: use CDN UNPKG [[sample](./jsmind-unpkg.html)]

```html
<link type="text/css" rel="stylesheet" href="//unpkg.com/jsmind@0.8.1/style/jsmind.css"/>

<script src="//unpkg.com/jsmind@0.8.1/es6/jsmind.js"></script>
<script src="//unpkg.com/npm/jsmind@0.8.1/es6/jsmind.draggable-node.js"></script>
```

Option 3 for China: use China mirror of jsDeliver [[sample](./jsmind-jsdeliver-cn-mirror.html)]

```html
<link type="text/css" rel="stylesheet" href="//jsd.onmicrosoft.cn/npm/jsmind@0.8.1/style/jsmind.css"/>

<script src="//jsd.onmicrosoft.cn/npm/jsmind@0.8.1/es6/jsmind.js"></script>
<script src="//jsd.onmicrosoft.cn/npm/jsmind@0.8.1/es6/jsmind.draggable-node.js"></script>
```

Option 4: download the files from CDN, and reference local resource

```html
<link type="text/css" rel="stylesheet" href="<filePath>/jsmind@0.8.1/style/jsmind.css"/>

<script src="<filePath>/jsmind@0.8.1/es6/jsmind.js"></script>
<script src="<filePath>/jsmind@0.8.1/es6/jsmind.draggable-node.js"></script>
```

## Write scripts in the HTML file

```html
<script>
    let options = {
        container: 'jsmind_container',
        editable: true,
        theme: 'primary',
    };
    let jsmind_data = {
        // 3 formats are supported, docs: https://hizzgdev.github.io/jsmind/docs/
    };
    let jm = new jsMind(options);
    jm.show(jsmind_data);
</script>
```

## More

jsMind project home: <a href="https://github.com/hizzgdev/jsmind">https://github.com/hizzgdev/jsmind</a>
