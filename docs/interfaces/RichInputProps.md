# Interface: RichInputProps

Props of [RichInput](../API.md#experimental_richinput).

For other props not mentioned below will be passed to [input](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement).
`defaultValue` is omitted for simplicity of logic.

## Hierarchy

- `Omit`<`JSX.IntrinsicElements`[``"input"``], ``"children"``\>

  ↳ **`RichInputProps`**

## Table of contents

### Properties

- [children](RichInputProps.md#children)
- [autoHeight](RichInputProps.md#autoheight)
- [onSelectionChange](RichInputProps.md#onselectionchange)

## Properties

### children

• `Optional` **children**: [`Renderer`](../API.md#renderer)

Render function to create customized view from value.

This function should return ReactNodes which texts are positioned the same as textarea (see examples for detailed usage).

On the rendered nodes, currently limited event handlers will work.
- `onClick`
- `onMouseOver`
- `onMouseOut`
- `onMouseMove`
- `onMouseDown`
- `onMouseUp`

**`Default Value`**

```ts
undefined
```

#### Defined in

[src/input.tsx:120](https://github.com/inokawa/rich-textarea/blob/c7423d9/src/input.tsx#L120)

___

### autoHeight

• `Optional` **autoHeight**: `boolean`

If true, textarea height is automatically resized and height of style prop does not work. Set `maxHeight` to style prop if you need limit.

**`Default Value`**

```ts
undefined
```

#### Defined in

[src/input.tsx:125](https://github.com/inokawa/rich-textarea/blob/c7423d9/src/input.tsx#L125)

___

### onSelectionChange

• `Optional` **onSelectionChange**: (`pos`: [`CaretPosition`](../API.md#caretposition)) => `void`

#### Type declaration

▸ (`pos`): `void`

Called when selection in textarea changes. It gives position of caret at the time, which is useful to position menu.

##### Parameters

| Name | Type |
| :------ | :------ |
| `pos` | [`CaretPosition`](../API.md#caretposition) |

##### Returns

`void`

**`Default Value`**

```ts
undefined
```

#### Defined in

[src/input.tsx:130](https://github.com/inokawa/rich-textarea/blob/c7423d9/src/input.tsx#L130)
