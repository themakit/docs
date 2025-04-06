# Modal

The `Modal` component is used to display content in a dialog box that appears on top of the main content.

## Import

```tsx
import { Modal } from '@themakit/modal';
```

## Usage

### Basic Modal

```tsx
<Modal isOpen={true} onClose={() => console.log('Modal closed')}>
  <h1>Modal Title</h1>
  <p>This is the modal content.</p>
</Modal>
```

### Modal with Header and Footer

You can include a header and footer in the modal for better structure.

```tsx
<Modal isOpen={true} onClose={() => console.log('Modal closed')}>
  <Modal.Header>
    <h1>Modal Title</h1>
  </Modal.Header>
  <Modal.Body>
    <p>This is the modal content.</p>
  </Modal.Body>
  <Modal.Footer>
    <button onClick={() => console.log('Cancel clicked')}>Cancel</button>
    <button onClick={() => console.log('Confirm clicked')}>Confirm</button>
  </Modal.Footer>
</Modal>
```

### Centered Modal

You can center the modal on the screen using the `centered` prop.

```tsx
<Modal isOpen={true} centered onClose={() => console.log('Modal closed')}>
  <h1>Centered Modal</h1>
  <p>This modal is centered on the screen.</p>
</Modal>
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `isOpen`     | `boolean`           | `false`   | Whether the modal is open.                      |
| `onClose`    | `() => void`        | `null`    | Callback function triggered when the modal is closed. |
| `centered`   | `boolean`           | `false`   | Whether the modal is centered on the screen.    |

## Accessibility

- Modals use `role="dialog"` and `aria-labelledby`/`aria-describedby` for accessibility.
- Ensure the modal content is meaningful and accessible to all users.

## Theming

You can customize the appearance of the `Modal` component using the theme:

```tsx
const theme = {
  components: {
    Modal: {
      backgroundColor: '#fff',
      color: '#000',
      borderRadius: '8px',
      boxShadow: '0 4px 6px rgba(0, 0, 0, 0.1)',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).