# Alert

The `Alert` component is used to display important messages to users. It supports different variants to convey the purpose of the message, such as success, error, warning, or informational alerts.

## Import

```tsx
import { Alert } from '@themakit/alert';
```

## Usage

### Basic Alert

```tsx
<Alert variant="info">
  This is an informational alert.
</Alert>
```

### Variants

The `Alert` component supports multiple variants to indicate the type of message:

```tsx
<Alert variant="success">
  This is a success alert.
</Alert>

<Alert variant="error">
  This is an error alert.
</Alert>

<Alert variant="warning">
  This is a warning alert.
</Alert>

<Alert variant="info">
  This is an informational alert.
</Alert>
```

### Dismissible Alert

You can make alerts dismissible by adding a close button.

```tsx
<Alert variant="info" dismissible onClose={() => console.log('Alert closed')}>
  This is a dismissible alert.
</Alert>
```

### Alert with Custom Icon

You can customize the icon displayed in the alert.

```tsx
<Alert variant="info" icon={<CustomIcon />}>
  This is an alert with a custom icon.
</Alert>
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `variant`    | `'success' | 'error' | 'warning' | 'info'` | `'info'` | The type of alert to display.                   |
| `dismissible`| `boolean`           | `false`   | Whether the alert can be dismissed.             |
| `onClose`    | `() => void`        | `null`    | Callback function triggered when the alert is dismissed. |
| `icon`       | `ReactNode`         | `null`    | Custom icon to display in the alert.            |

## Accessibility

- Alerts use `role="alert"` to ensure they are announced by screen readers.
- Dismissible alerts include accessible labels for the close button.

## Theming

You can customize the appearance of the `Alert` component using the theme:

```tsx
const theme = {
  components: {
    Alert: {
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