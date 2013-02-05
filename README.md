sublime-ext-snippets
====================

Snippets for Sencha ExtJS Programming in Sublime Text 2

Install
-------

### Mac OS X

	git clone git://github.com/clrhodes/sublime-ext-snippets.git ~/Library/Application Support/Sublime Text 2/Packages/SenchaExt

### Linux

	git clone git://github.com/clrhodes/sublime-ext-snippets.git ~/.config/sublime-text-2/Packages/SenchaExt

### Windows

    git clone git://github.com/clrhodes/sublime-ext-snippets.git %userprofile%\AppData\Roaming\Sublime Text 2\Packages\SenchaExt

Sencha ExtJS Snippets
--------

### [xapp] Ext.application
```Ext.application({
   name: '$1',
   autoCreateViewport: true,
   controllers: ['$2'],
   launch: function() {
        $3
        console.log('Application launched.');
   }
});
```


### [xview] Ext.Container 

```
Ext.define('${1:MyApp}.view.${TM_FILENAME/(.*)[.](.*)/$1/g}', {
    extend: '${2:Ext.Container}',
    layout: {
        type: '${3:auto}'
    },
    items: [{
        $4
    }]
});
```


### [xcontrol] Ext.app.Controller

```
Ext.define('${1:MyApp}.controller.${TM_FILENAME/(.*)[.](.*)/$1/g}', {
    extend: 'Ext.app.Controller',
    models: [],
    stores: [],
    views: [],
    refs: [],
    init: function() {
        this.control({
            $2
        });
    }
});
```


### [xmodel] Ext.data.Model

```
Ext.define('${1:MyApp}.model.${TM_FILENAME/(.*)[.](.*)/$1/g}', {
    extend: 'Ext.data.Model',
    idProperty: '${2:id}',
    fields: [{
        name: '${3:id}',
        type: '${4:int}'
    }]
});
```


### [xstore] Ext.data.Store

```
Ext.define('${1:MyApp}.store.${TM_FILENAME/(.*)[.](.*)/$1/g}', {
    extend: 'Ext.data.Store',
    model: '${2}',
    autoLoad: ${3:true},
    remoteSort: ${4:true},
    remoteFilter: ${5:true}
});
```


Author
--------

Christopher Rhodes

License
--------

Copyright 2012, Christopher Rhodes <clrhodes@gmail.com>

MIT
