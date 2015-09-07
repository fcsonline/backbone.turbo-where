# backbone.turbo-where

Backbone Collections with indexes.

## Usage

```js
var MyCollection = Backbone.Collection.extend({
  initialize: function () {
    TurboWhere.setupIndexes(this, ['foreign_key']);
  }
});

var my_collection = new MyCollection();

my_collection.reset([
  {id: 1, foreign_key: 11},
  {id: 2, foreign_key: 11},
  {id: 3, foreign_key: 11},
  {id: 4, foreign_key: 22},
  {id: 5, foreign_key: 22},
  {id: 6, foreign_key: 22}
]);

my_collection.where({foreign_key: 22}) // <= will use an index
```

