# Quick Start

Get started with ThemaKit in just a few steps! Follow this guide to set up and start using the library in your React project.

## Installation

First, install the ThemaKit library and its peer dependencies:

```bash
npm install @themakit/core @themakit/theme react react-dom
```

Or, if you use Yarn:

```bash
yarn add @themakit/core @themakit/theme react react-dom
```

## Setting Up the Theme

Wrap your application with the `ThemeProvider` to apply the ThemaKit theme:

```tsx
import React from 'react';
import ReactDOM from 'react-dom';
import { ThemeProvider, defaultTheme } from '@themakit/theme';

const App = () => (
  <ThemeProvider theme={defaultTheme}>
    <h1>Hello, ThemaKit!</h1>
  </ThemeProvider>
);

ReactDOM.render(<App />, document.getElementById('root'));
```

## Using Components

Start using ThemaKit components in your application. For example, here’s how to use a `Button`:

```tsx
import React from 'react';
import { Button } from '@themakit/core';

const App = () => (
  <div>
    <Button variant="primary">Click Me</Button>
  </div>
);

export default App;
```

## Customizing the Theme

You can customize the default theme to match your design requirements:

```tsx
import { ThemeProvider, createTheme } from '@themakit/theme';

const customTheme = createTheme({
  palette: {
    primary: '#4caf50',
    accent: '#ff5722',
  },
});

const App = () => (
  <ThemeProvider theme={customTheme}>
    <h1>Custom Theme</h1>
  </ThemeProvider>
);
```

For more details on theming, see the [Theming Guide](../../theming/overview).

## Next Steps

- Explore the [Components](../../components/layout/container.md) section to learn about all available components.
- Check out the [Theming Guide](../../theming/overview) to customize your application’s look and feel.