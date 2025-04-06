# Flex

The `Flex` component is used to create flexible layouts using CSS flexbox.

## Import

```tsx
import { Flex } from '@themakit/flex';
```

## Usage

### Basic Flex

```tsx
<Flex>
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</Flex>
```

### Align Items

You can align items along the cross axis using the `align` prop.

```tsx
<Flex align="center">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</Flex>
```

### Justify Content

You can distribute items along the main axis using the `justify` prop.

```tsx
<Flex justify="space-between">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</Flex>
```

### Direction

You can change the direction of the flex items using the `direction` prop.

```tsx
<Flex direction="column">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</Flex>
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `align`      | `'flex-start' | 'center' | 'flex-end' | 'stretch'` | `'stretch'` | Alignment of items along the cross axis.        |
| `justify`    | `'flex-start' | 'center' | 'flex-end' | 'space-between' | 'space-around'` | `'flex-start'` | Distribution of items along the main axis.      |
| `direction`  | `'row' | 'column'`   | `'row'`   | Direction of the flex items.                    |
| `gap`        | `string | number`   | `0`       | Gap between flex items.                         |

## Accessibility

- The `Flex` component is a layout tool and does not have specific accessibility features.
- Ensure the content inside the flex container is accessible.

## Theming

You can customize the appearance of the `Flex` component using the theme:

```tsx
const theme = {
  components: {
    Flex: {
      gap: '16px',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).