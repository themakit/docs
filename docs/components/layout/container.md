# TextField

The `TextField` component is used to capture user input in the form of text.

## Import

```tsx
import { TextField } from '@themakit/textfield';
```

## Usage

### Basic TextField

```tsx
<TextField placeholder="Enter your name" />
```

### Controlled TextField

You can control the value of the `TextField` using the `value` and `onChange` props.

```tsx
const [value, setValue] = React.useState('');

<TextField
  value={value}
  onChange={(e) => setValue(e.target.value)}
  placeholder="Enter your email"
/>;
```

### TextField with Label

You can add a label to the `TextField` for better context.

```tsx
<TextField label="Name" placeholder="Enter your name" />
```

### Disabled TextField

You can disable the `TextField` using the `disabled` prop.

```tsx
<TextField label="Disabled" placeholder="Cannot type here" disabled />
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `value`      | `string`            | `''`      | The current value of the text field.            |
| `onChange`   | `(event: React.ChangeEvent<HTMLInputElement>) => void` | `null` | Callback triggered when the value changes.      |
| `placeholder`| `string`            | `''`      | Placeholder text displayed inside the text field. |
| `label`      | `string`            | `null`    | Label displayed above the text field.           |
| `disabled`   | `boolean`           | `false`   | Whether the text field is disabled.             |

## Accessibility

- The `TextField` component uses native `<input>` elements for accessibility.
- Ensure the `label` prop provides meaningful context for screen readers.

## Theming

You can customize the appearance of the `TextField` component using the theme:

```tsx
const theme = {
  components: {
    TextField: {
      backgroundColor: '#fff',
      borderColor: '#ccc',
      focusBorderColor: '#4caf50',
    },
  },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).