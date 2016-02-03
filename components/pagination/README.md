# Pagination

## Options

| Option | Description | Type | Default value |
| ------ | ----------- | ---- | ------------- |
| target | The table element to fire events at | Element | null |
| sizing | Sets the size of the pagination buttons: "sm", "lg" | string | null |
| pager | Renders the more simplified "Pager" style | Boolean | false |
| pagerAlign | Aligns the pager buttons to the sides, when using the `pager` option  | Boolean | false |
| prev  | Turns the "previous" button on/off | Boolean | false |
| next  | Turns the "next" button on/off | Boolean | false |
| first | Turns the "first" button on/off | Boolean | false |
| last  | Turns the "last" button on/off | Boolean | false |
| pageStart | The first page number in a range to be displayed (ignored when using the `pageList` option) | Integer | null |
| pageEnd  | The last page number in a range to be displayed (ignored when using the `pageList` option) | Integer | null |
| pageList  | The list of page links to generate | Array | [] |

## Methods

| Method | Description | Parameters | Returns |
| ------ | ----------- | ---------- | ------- |
| destroy | Reverts the DOM element to its inital state | N/A | void |
| render | Renders the pagination element | N/A | `this` |
| set[OptionName] | Sets an option -i.e. `$().setTarget(el)` | mixed | `this` |
| get[OptionName] | Gets the current value of an option -i.e. `$().getTarget()` | N/A | mixed |

## Events

| Event | Description |
| ----- | ----------- |
| all.bs.pagination   | Fires before any `*.bs.pagination` event            |
| prev.bs.pagination  | This event fires when the "prev" button is clicked  |
| next.bs.pagination  | This event fires when the "next" button is clicked  |
| first.bs.pagination | This event fires when the "first" button is clicked |
| last.bs.pagination  | This event fires when the "last" button is clicked  |
| page.bs.pagination  | This event fires when any "page" button is clicked  |
