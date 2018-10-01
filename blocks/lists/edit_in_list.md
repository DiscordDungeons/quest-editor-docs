# Edit List Blocks

These all apply to the `insert at` option aswell.

# Set In List Block

![Set In List](../../images/list/set_list_index.jpg)

The set in list block sets the item in the list with the specified index to the specified value.

### Generated Code

```js
var list;

list[index] = <value>;

```

# Set In List From End Block

![Set In List From End](../../images/list/set_list_index_from_end.jpg)

The set in list from end block sets the item in the list with the specified index from the end to the specified value.

### Generated Code


```js
var list;

list[list.length - <index>] = <value>;
```

# Set First In List Block

![Set First In List](../../images/list/set_first_item.jpg)

The set first in list block sets the first item in the list to the specified value.

### Generated Code


```js
var list;

list[0] = <value>;
```

# Set Last In List Block

![Set Last In List](../../images/list/set_last_item.jpg)

The set last in list block sets the last item in the list to the specified value.

### Generated Code


```js
var list;

list[list.length - 1] = <value>;
```


