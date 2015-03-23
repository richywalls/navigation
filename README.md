## Smart TV navigation

Keyboard navigation for Smart TV applications

## Download
 
[navigation.zip](https://github.com/ahiipsa/navigation/zipball/master)

[navigation.tar.gz](https://github.com/ahiipsa/navigation/tarball/master)

## Install with Bower

`bower install navigation`

## Install with npm

todo...
 
## Attributes

- `nv-scope` create scope
- `nv-scope-current` activate scope after bootstrap
- `nv-el` navigation element
- `nv-el-current` activate after bootstrap

### Example
```html

    <div nv-scope="menu" nv-scope-current>
        <div nv-el nv-el-current>Element 1</div>
        <div nv-el>Element 2</div>
        <div nv-el>Element 3</div>
    </div>
    
```

## Class

- `nv-scope` add for scopes element
- `nv-scope-current` add for current scope element
- `nv-el` add for navigation elements
- `nv-el-current` add for current navigation element

```html

    <div nv-scope="menu" class="nv-scope nv-scope-current" nv-scope-current>
        <div nv-el nv-el-current class="nv-el nv-el-current">Element 1</div>
        <div nv-el class="nv-el">Element 2</div>
        <div nv-el class="nv-el">Element 3</div>
    </div>
    
```

## Event listener

```js

document.body.addEventListener('nv-left', function (event) {
    // logic
});

```

### Default events

nv-left, nv-up, nv-right, nv-down, nv-enter, nv-back, nv-red, nv-green, nv-yellow, nv-blue, nv-rw, nv-stop, nv-play, nv-ff, nv-ch_up, nv-ch_down, nv-info, nv-mic

or use:

```js

var keyMapping = navigation.getKeyMapping();

```

### Custom events and key mapping

```js

// example keyCode: 'eventName'

var keyMapping = {
    403: 'red',
    404: 'green',
    405: 'yellow',
    406: 'blue',
    412: 'rw',
    413: 'stop',
    415: 'play',
    417: 'ff',
    33:  'ch_up',
    34:  'ch_down',
    457: 'info',
    461: 'back', // return
    1015:'mic'
};

navigation.addKeyMapping(keyMapping);
 
document.body.addEventListener('nv-play', function (event) {
    // logic
});

```