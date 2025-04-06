# Keyframes

The `Keyframes` utility in ThemaKit allows you to define and use CSS animations in your components.

## Import

```tsx
import { keyframes } from '@themakit/animations';
```

## Creating Keyframes

You can create custom keyframes using the `keyframes` utility.

```tsx
import { keyframes } from '@themakit/animations';

const fadeIn = keyframes`
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
`;
```

## Using Keyframes in Components

Apply the keyframes to a component using the `animation` property.

```tsx
import styled from 'styled-components';
import { keyframes } from '@themakit/animations';

const fadeIn = keyframes`
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
`;

const AnimatedDiv = styled.div`
  animation: ${fadeIn} 2s ease-in-out;
`;

const App = () => (
  <AnimatedDiv>
    <p>This content fades in!</p>
  </AnimatedDiv>
);
```

## Props

| Prop         | Type                | Default   | Description                                      |
|--------------|---------------------|-----------|--------------------------------------------------|
| `keyframes`  | `string`            | `null`    | The keyframes definition for the animation.     |
| `duration`   | `string`            | `'1s'`    | The duration of the animation.                  |
| `timing`     | `string`            | `'ease'`  | The timing function for the animation.          |

## Accessibility

- Use animations sparingly to avoid overwhelming users.
- Provide alternatives or disable animations for users with motion sensitivity.

## Next Steps

- Learn about [Transitions](transitions.md) for simpler animations.
- Explore the [Theming Guide](../theming/overview.md) to customize animations.