# Button

The Button component is used to trigger an action or event, such as submitting a form, opening a dialog, canceling an action, or performing a delete operation.

## Import

```tsx
import { Button } from '@themakit/button';
```

## Usage

```tsx
<Button variant="primary">Click Me</Button>
```

## Examples

### Button Variants

ThemaKit buttons come in several variants to indicate different levels of emphasis.

```tsx
<Button variant="primary">Primary</Button>
<Button variant="secondary">Secondary</Button>
<Button variant="outline">Outline</Button>
<Button variant="text">Text</Button>
<Button variant="destructive">Delete</Button>
```

### Button Sizes

Buttons are available in different sizes to fit your design needs.

```tsx
<Button size="sm">Small</Button>
<Button size="md">Medium</Button>
<Button size="lg">Large</Button>
```

### Button States

```tsx
<Button>Default</Button>
<Button disabled>Disabled</Button>
<Button loading>Loading</Button>
```

### With Icon

```tsx
<Button startIcon={<IconName />}>Start Icon</Button>
<Button endIcon={<IconName />}>End Icon</Button>
<Button icon={<IconName />} aria-label="Icon only button" />
```

### Full Width

```tsx
<Button fullWidth>Full Width Button</Button>
```

### Props

| Prop      | Type                          | Default     | Description                     |
| --------- | ----------------------------- | ----------- | ------------------------------- |
| `variant` | `'primary' | 'secondary' | 'outline' | 'text' | 'destructive'` | `'primary'`  | The variant of the button      |
| `size`    | `'sm' | 'md' | 'lg'`             | `'md'`      | The size of the button          |
| `disabled` | `boolean` | `false` | Whether the button is disabled |
| `loading` | `boolean` | `false` | Whether the button is in a loading state |
| `fullWidth` | `boolean` | `false` | If true, the button will take up the full width of its container |
| `startIcon` | `ReactNode` |       | Icon to display at the start of the button | 
| `endIcon` | `ReactNode` |     | Icon to display at the end of the button |
| `icon` | `ReactNode` |        | Icon to display (for icon-only buttons) |
| `type` | `'button' | 'submit' | 'reset'` | `'button'` | The HTML button type |
| `onClick` | `(event: React.MouseEvent<HTMLButtonElement>) => void` |      | Function called when the button is clicked |
| `ref` | `React.Ref<HTMLButtonElement>` |      | Ref forwarded to the button element |

The Button component also accepts all props that can be passed to a standard HTML button element.

### Accessibility

- When using the `icon` prop without text, always provide an `aria-label` to ensure the button is accessible to screen reader users.
- The Button component handles keyboard focus and uses appropriate ARIA attributes based on its state.
- When in a `loading` state, the button will be marked with `aria-busy="true"`.

### Theming

You can customize the appearance of the Button component using the theme:

```tsx
// Example theme customization
const theme = {
    components: {
        Button: {
            variants: {
                primary: {
                    backgroundColor: '#0066ff',
                    color: 'white',
                    // ... other styles
                },
            },
            sizes: {
                sm: {
                    padding: '0.25rem 0.5rem',
                    fontSize: '0.875rem',
                },
                // ... other sizes
            },
        },
    },
};
```

For more information on theming, see the [Theming Guide](../../../theming/overview).