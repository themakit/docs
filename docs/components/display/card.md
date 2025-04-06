# Card

The `Card` component is a flexible and extensible container for displaying content in a structured layout.

## Import

```tsx
import { Card } from '@themakit/card';
```

## Usage

### Basic Card

```tsx
<Card>
  <h3>Card Title</h3>
  <p>This is some content inside the card.</p>
</Card>
```

### Card with Header and Footer

You can add a header and footer to the card for better structure.

```tsx
<Card>
  <Card.Header>
    <h3>Card Header</h3>
  </Card.Header>
  <Card.Body>
    <p>This is the main content of the card.</p>
  </Card.Body>
  <Card.Footer>
    <button>Action</button>
  </Card.Footer>
</Card>
```

### Card with Image

You can include an image in the card.

```tsx
<Card>
  <img src="https://via.placeholder.com/150" alt="Card Image" />
  <Card.Body>
    <h3>Card Title</h3>
    <p>This is some content inside the card.</p>
  </Card.Body>
</Card>
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `elevation`  | `number`            | `1`       | The elevation level of the card (e.g., shadow depth). |
| `bordered`   | `boolean`           | `false`   | Whether the card has a border.                  |

## Accessibility

- Cards are accessible by default and can be used as containers for any content.
- Ensure the content inside the card is meaningful and accessible.

## Theming

You can customize the appearance of the `Card` component using the theme:

```tsx
const theme = {
  components: {
    Card: {
      backgroundColor: '#fff',
      color: '#000',
      borderRadius: '8px',
      boxShadow: '0 2px 4px rgba(0, 0, 0, 0.1)',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).