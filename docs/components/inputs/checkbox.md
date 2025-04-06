# Checkbox

The `Checkbox` component is used to allow users to select one or more options from a set.

## Import

```tsx
import { Checkbox } from '@themakit/checkbox';
```

## Usage

### Basic Checkbox

```tsx
<Checkbox label="Accept Terms and Conditions" />
```

### Controlled Checkbox

You can control the state of the checkbox using the `checked` and `onChange` props.

```tsx
const [checked, setChecked] = React.useState(false);

<Checkbox
  label="Subscribe to newsletter"
  checked={checked}
  onChange={(e) => setChecked(e.target.checked)}
/>;
```

### Disabled Checkbox

You can disable the checkbox using the `disabled` prop.

```tsx
<Checkbox label="Disabled Checkbox" disabled />
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `label`      | `string`            | `null`    | The label displayed next to the checkbox.       |
| `checked`    | `boolean`           | `false`   | Whether the checkbox is checked (controlled).   |
| `defaultChecked` | `boolean`       | `false`   | Whether the checkbox is initially checked.      |
| `disabled`   | `boolean`           | `false`   | Whether the checkbox is disabled.               |
| `onChange`   | `(event: React.ChangeEvent<HTMLInputElement>) => void` | `null` | Callback triggered when the checkbox state changes. |

## Accessibility

- The `Checkbox` component uses native `<input type="checkbox">` for accessibility.
- Ensure the `label` prop provides meaningful context for screen readers.

## Theming

You can customize the appearance of the `Checkbox` component using the theme:

```tsx
const theme = {
  components: {
    Checkbox: {
      color: '#4caf50',
      disabledColor: '#9e9e9e',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).