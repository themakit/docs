# Toast

The `Toast` component is used to display brief, auto-expiring messages to notify users of specific actions or events.

## Import

```tsx
import { Toast } from '@themakit/toast';
```

## Usage

### Basic Toast

```tsx
<Toast message="This is a toast notification" />
```

### Variants

The `Toast` component supports multiple variants to indicate the type of message:

```tsx
<Toast variant="success" message="Operation successful!" />
<Toast variant="error" message="An error occurred!" />
<Toast variant="warning" message="Warning: Check your input!" />
<Toast variant="info" message="This is an informational toast." />
```

### Toast with Custom Duration

You can specify how long the toast should remain visible using the `duration` prop (in milliseconds).

```tsx
<Toast message="This toast will disappear in 5 seconds" duration={5000} />
```

### Toast with Action

You can include an action button in the toast.

```tsx
<Toast
  message="File uploaded successfully"
  action={{ label: 'Undo', onClick: () => console.log('Undo clicked') }}
/>
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `message`    | `string`            | `null`    | The message to display in the toast.            |
| `variant`    | `'success' | 'error' | 'warning' | 'info'` | `'info'` | The type of toast to display.                   |
| `duration`   | `number`            | `3000`    | Duration in milliseconds before the toast disappears. |
| `action`     | `{ label: string; onClick: () => void }` | `null` | Action button with a label and click handler.   |

## Accessibility

- Toasts use `role="status"` to ensure they are announced by screen readers.
- Ensure the `message` prop provides meaningful information for all users.

## Theming

You can customize the appearance of the `Toast` component using the theme:

```tsx
const theme = {
  components: {
    Toast: {
      success: {
        backgroundColor: '#d4edda',
        color: '#155724',
      },
      error: {
        backgroundColor: '#f8d7da',
        color: '#721c24',
      },
      warning: {
        backgroundColor: '#fff3cd',
        color: '#856404',
      },
      info: {
        backgroundColor: '#d1ecf1',
        color: '#0c5460',
      },
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).