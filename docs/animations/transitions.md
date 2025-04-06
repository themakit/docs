# Transitions

The `Transitions` utility in ThemaKit allows you to create smooth animations for property changes.

## Import

```tsx
import { transition } from '@themakit/animations';
```

## Creating Transitions

You can create custom transitions using the `transition` utility.

```tsx
import styled from 'styled-components';

const Button = styled.button`
  background-color: #4caf50;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: #388e3c;
  }
`;

const App = () => (
  <Button>Hover Me</Button>
);
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `property`   | `string`            | `'all'`   | The CSS property to apply the transition to.    |
| `duration`   | `string`            | `'0.3s'`  | The duration of the transition.                 |
| `timing`     | `string`            | `'ease'`  | The timing function for the transition.         |

## Accessibility

- Ensure transitions are smooth and do not distract users.
- Provide alternatives or disable transitions for users with motion sensitivity.

## Next Steps

- Learn about [Keyframes](keyframes.md) for more complex animations.
- Explore the [Theming Guide](../theming/overview.md) to customize transitions.