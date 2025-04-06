# Grid

The `Grid` component is used to create responsive layouts with rows and columns.

## Import

```tsx
import { Grid, GridItem } from '@themakit/grid';
```

## Usage

### Basic Grid

```tsx
<Grid>
  <GridItem span={6}>Column 1</GridItem>
  <GridItem span={6}>Column 2</GridItem>
</Grid>
```

### Responsive Grid

You can define different column spans for different screen sizes.

```tsx
<Grid>
  <GridItem span={12} md={6} lg={4}>
    Column 1
  </GridItem>
  <GridItem span={12} md={6} lg={4}>
    Column 2
  </GridItem>
  <GridItem span={12} md={6} lg={4}>
    Column 3
  </GridItem>
</Grid>
```

### Nested Grid

You can nest grids inside grid items.

```tsx
<Grid>
  <GridItem span={12}>
    <Grid>
      <GridItem span={6}>Nested Column 1</GridItem>
      <GridItem span={6}>Nested Column 2</GridItem>
    </Grid>
  </GridItem>
</Grid>
```

## Props

### `Grid`

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `gap`        | `number | string`   | `0`       | The gap between grid items.                     |

### `GridItem`

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `span`       | `number`            | `12`      | The number of columns the item spans.           |
| `md`         | `number`            | `null`    | The span for medium-sized screens.              |
| `lg`         | `number`            | `null`    | The span for large-sized screens.               |

## Accessibility

- The `Grid` component is a layout tool and does not have specific accessibility features.
- Ensure the content inside grid items is accessible.

## Theming

You can customize the appearance of the `Grid` component using the theme:

```tsx
const theme = {
  components: {
    Grid: {
      gap: '16px',
    },
    GridItem: {
      padding: '8px',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).