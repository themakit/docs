# ThemaKit

**Modern UI Components for React**

Build beautiful, consistent interfaces with our themeable component library.

---

## Installation

Get started with ThemaKit in your React project:

[Installation →](getting-started/installation.md)

---

## Features

- **Fully Customizable:** Theme every aspect of your components with our powerful theming system.
- **Type-Safe:** Built with TypeScript for a robust development experience.
- **Accessible:** WCAG 2.1 compliant components out of the box.
- **Modern Stack:** React 18+, CSS-in-JS, and zero jQuery dependencies.

---

## Quick Example

```tsx
import { ThemeProvider } from '@themakit/core';
import { Button } from '@themakit/button';
import { defaultTheme } from '@themakit/theme';

function App() {
    return (
        <ThemeProvider theme={defaultTheme}>
            <Button variant="primary">Get Started</Button>
        </ThemeProvider>
    );
}
```