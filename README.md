# core.loader.hooks

loads hooks from plugin definition


```js
let core = new require('core.constructor')();
 
core.plugin(
    require('core.loader.hooks')
);

// plugins can now declare actions on the plugin definition object:
core.plugin({
    name: 'test',
    hooks: [
        {
            channel: 'someChannel',
            hook(data, done){
                done(data);
            }
        }
    ]
});

// run the newly created action
core.fire('someChannel', { some: 'data' }, () => { /* done */ })

```
