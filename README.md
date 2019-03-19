# Grid

A little collection of Vue components to use with our grid. 



### Install

```npm install @sil/grid --save```

### Use

```js
import Grid from "@sil/grid";
const Row = Grid.row;
const Column = Grid.column;

export default {
  name: "app",
  components: {
    Column,
    Row
  }
}
```

### Usage

#### Row
Instead of writing:
`<div class="row center"></div>`

You can write:
`<row center></row>`

#### Column
Instead of writing:
`<div class="column small-full medium-two-third large-half"></div>`

You can write:
`<column medium="2:3" large="half"></column>`

Which makes it easier and faster to write and see what is happening. 



