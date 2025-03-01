# CheckPicker

Used for multiple data selection, support grouping.

## Import

<!--{include:(components/check-picker/fragments/import.md)}-->

## Examples

### Basic

<!--{include:`basic.md`}-->

### With a label

<!--{include:`with-label.md`}-->

### Appearance

<!--{include:`appearance.md`}-->

### Size

<!--{include:`size.md`}-->

### Sticky

Set the `sticky` property to put the selected in the options to the top.

<!--{include:`sticky.md`}-->

### Block

<!--{include:`block.md`}-->

### Group

<!--{include:`group.md`}-->

### Placement

<!--{include:`placement.md`}-->

> Tip: When set to `auto*`, try to scroll the page, or change the browser size, it will automatically appear in the right place.

### Custom options

<!--{include:`custom.md`}-->

### Disabled and read only

<!--{include:`disabled.md`}-->

### Disabled Search

<!--{include:`searchable.md`}-->

### Extra footer

Customize a select all function.

<!--{include:`extra-footer.md`}-->

### Async

<!--{include:`async.md`}-->

### Container and prevent overflow

<!--{include:`container.md`}-->

### Controlled

<!--{include:`controlled.md`}-->

## Accessibility

Learn more in [Accessibility](/guide/accessibility).

## Props

### `<CheckPicker>`

| Property           | Type`(Default)`                                                                                    | Description                                                 |
| ------------------ | -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| appearance         | 'default' &#124; 'subtle' `('default')`                                                            | Set picker appearence                                       |
| block              | boolean                                                                                            | Blocking an entire row                                      |
| classPrefix        | string `('picker')`                                                                                | The prefix of the component CSS class                       |
| cleanable          | boolean `(true)`                                                                                   | Whether the selected value can be cleared                   |
| container          | HTMLElement &#124; (() => HTMLElement)                                                             | Sets the rendering container                                |
| countable          | boolean `(true)`                                                                                   | Whether display selected items count                        |
| data \*            | [ItemDataType][item][]                                                                             | The data of component                                       |
| defaultValue       | [ValueType][value]                                                                                 | Default values of the selected items                        |
| disabled           | boolean                                                                                            | Whether disabled component                                  |
| disabledItemValues | [ValueType][value]                                                                                 | Disable item by value                                       |
| groupBy            | string                                                                                             | Set group condition key in data                             |
| label              | ReactNode                                                                                          | A label displayed at the beginning of toggle button         |
| labelKey           | string `('label')`                                                                                 | Set label key in data                                       |
| listProps          | [ListProps][listprops]                                                                             | List-related properties in `react-virtualized`              |
| locale             | [PickerLocaleType](/guide/i18n/#pickers)                                                           | Locale text                                                 |
| menuMaxHeight      | number `(320)`                                                                                     | The max height of Dropdown                                  |
| menuClassName      | string                                                                                             | A css class to apply to the Menu DOM node.                  |
| menuStyle          | CSSProperties                                                                                      | A style to apply to the Menu DOM node.                      |
| onChange           | (value: [ValueType][value], event) => void                                                         | Callback fired when value change                            |
| onClean            | (event:SyntheticEvent) => void                                                                     | Callback fired when value clean                             |
| onClose            | () => void                                                                                         | Callback fired when close component                         |
| onEnter            | () => void                                                                                         | Callback fired before the overlay transitions in            |
| onEntered          | () => void                                                                                         | Callback fired after the overlay finishes transitioning in  |
| onEntering         | () => void                                                                                         | Callback fired as the overlay begins to transition in       |
| onExit             | () => void                                                                                         | Callback fired right before the overlay transitions out     |
| onExited           | () => void                                                                                         | Callback fired after the overlay finishes transitioning out |
| onExiting          | () => void                                                                                         | Callback fired as the overlay begins to transition out      |
| onGroupTitleClick  | (event) => void                                                                                    | Callback fired when click the group title                   |
| onOpen             | () => void                                                                                         | Callback fired when open component                          |
| onSearch           | (searchKeyword:string, event) => void                                                              | Callback fired when search                                  |
| onSelect           | (value: [ValueType][value], item: [ItemDataType][item] , event) => void                            | Callback fired when item is selected                        |
| open               | boolean                                                                                            | Whether open the component                                  |
| placeholder        | ReactNode `('Select')`                                                                             | Setting placeholders                                        |
| placement          | [Placement](#code-ts-placement-code)`('bottomStart')`                                              | The placement of component                                  |
| preventOverflow    | boolean                                                                                            | Prevent floating element overflow                           |
| renderExtraFooter  | () => ReactNode                                                                                    | Custom render extra footer                                  |
| renderMenu         | (menu:ReactNode) => ReactNode                                                                      | Customizing the Rendering Menu list                         |
| renderMenuGroup    | (groupTitle:ReactNode, item:[ItemDataType][item]) => ReactNode                                     | Custom render menu group                                    |
| renderMenuItem     | (label:ReactNode, item: [ItemDataType][item]) => ReactNode                                         | Custom render menu items                                    |
| renderValue        | (value: [ValueType][value], items: [ItemDataType][item][], selectedElement:ReactNode) => ReactNode | Custom render selected items                                |
| searchBy           | (keyword: string, label: ReactNode, item: ItemDataType) => boolean                                 | Custom search rules                                         |
| searchable         | boolean `(true)`                                                                                   | Whether dispaly search input box                            |
| size               | 'lg' &#124; 'md' &#124; 'sm' &#124; 'xs' `('md')`                                                  | A picker can have different sizes                           |
| sort               | (isGroup: boolean) => (a: any, b: any) => number                                                   | Sort options                                                |
| sticky             | boolean                                                                                            | Top the selected option in the options                      |
| toggleAs           | ElementType `('a')`                                                                                | You can use a custom element for this component             |
| value              | [ValueType][value]                                                                                 | Specifies the values of the selected items (Controlled)     |
| valueKey           | string `('value')`                                                                                 | Set value key in data                                       |
| virtualized        | boolean                                                                                            | Whether using Virtualized List                              |
| caretAs            | ElementType                                                                                        | Custom component for the caret icon                         |

[listprops]: https://github.com/bvaughn/react-virtualized/blob/master/docs/List.md#prop-types

<!--{include:(_common/types/item-data-type.md)}-->
<!--{include:(_common/types/placement.md)}-->

### `ts:ValueType`

```ts
type ValueType = (string | number)[];
```

[item]: #code-ts-item-data-type-code
[value]: #code-ts-value-type-code
