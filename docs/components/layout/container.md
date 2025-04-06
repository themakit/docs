# Container

The `Container` component is used to center and constrain the width of your content.

## Import

```tsx
import { Container } from '@themakit/container';
```

## Usage

### Basic Container

```tsx
<Container>
  <p>This content is inside a container.</p>
</Container>
```

### Fluid Container

You can make the container fluid (full-width) using the `fluid` prop.

```tsx
<Container fluid>
  <p>This content spans the full width of the screen.</p>
</Container>
```

### Custom Max Width

You can specify a custom maximum width for the container.

```tsx
<Container maxWidth="800px">
  <p>This content is constrained to a maximum width of 800px.</p>
</Container>
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `fluid`      | `boolean`           | `false`   | Whether the container spans the full width of the screen. |
| `maxWidth`   | `string`            | `'1200px'`| The maximum width of the container.             |

## Accessibility

- The `Container` component is a layout tool and does not have specific accessibility features.
- Ensure the content inside the container is accessible.

## Theming

You can customize the appearance of the `Container` component using the theme:

```tsx
const theme = {
  components: {
    Container: {
      maxWidth: '1200px',
      padding: '16px',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).