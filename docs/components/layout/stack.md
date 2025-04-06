# Stack

The `Stack` component is used to arrange items in a vertical or horizontal stack with consistent spacing.

## Import

```tsx
import { Stack } from '@themakit/stack';
```

## Usage

### Vertical Stack

```tsx
<Stack spacing="16px">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</Stack>
```

### Horizontal Stack

You can arrange items horizontally using the `direction` prop.

```tsx
<Stack direction="row" spacing="16px">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</Stack>
```

### Align Items

You can align items along the cross axis using the `align` prop.

```tsx
<Stack direction="row" align="center" spacing="16px">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</Stack>
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `direction`  | `'row' | 'column'`   | `'column'`| Direction of the stack (vertical or horizontal). |
| `spacing`    | `string | number`   | `0`       | Spacing between items in the stack.             |
| `align`      | `'flex-start' | 'center' | 'flex-end' | 'stretch'` | `'stretch'` | Alignment of items along the cross axis.        |

## Accessibility

- The `Stack` component is a layout tool and does not have specific accessibility features.
- Ensure the content inside the stack is accessible.

## Theming

You can customize the appearance of the `Stack` component using the theme:

```tsx
const theme = {
  components: {
    Stack: {
      spacing: '16px',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).