# Animations Overview

ThemaKit provides powerful animation utilities to enhance the user experience with smooth transitions and dynamic effects. These utilities include `Keyframes` for complex animations and `Transitions` for simple property changes.

## Key Features

- **Keyframes**: Define custom animations using CSS keyframes.
- **Transitions**: Create smooth animations for property changes.
- **Theming Support**: Customize animations to match your application's theme.
- **Accessibility**: Ensure animations are user-friendly and respect motion preferences.

## Why Use Animations?

Animations can improve the user experience by:

- Drawing attention to important elements.
- Providing visual feedback for user interactions.
- Making transitions between states feel smooth and natural.

## Getting Started

### Keyframes

Use `Keyframes` for creating complex animations like fades, slides, and rotations.

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

Learn more in the [Keyframes](keyframes.md) section.

### Transitions

Use `Transitions` for animating property changes like color, size, or position.

```tsx
import styled from 'styled-components';

const Button = styled.button`
  background-color: #4caf50;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: #388e3c;
  }
`;
```

Learn more in the [Transitions](transitions.md) section.

## Accessibility

- Respect user preferences for reduced motion by using the `prefers-reduced-motion` media query.
- Avoid excessive or distracting animations.

```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation: none;
    transition: none;
  }
}
```

## Next Steps

- Dive into [Keyframes](keyframes.md) for advanced animations.
- Explore [Transitions](transitions.md) for simple and effective animations.
- Check out the [Theming Guide](../theming/overview.md) to customize animations for your application.