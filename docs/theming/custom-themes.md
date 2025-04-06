# Custom Themes

ThemaKit allows you to create custom themes to match your application's design requirements.

## Creating a Custom Theme

You can create a custom theme using the `createTheme` function.

```tsx
import { createTheme, ThemeProvider } from '@themakit/theme';

const customTheme = createTheme({
  palette: {
    primary: '#4caf50',
    accent: '#ff5722',
    background: '#f5f5f5',
    text: '#212121',
  },
  components: {
    Button: {
      backgroundColor: '#4caf50',
      color: '#fff',
      hoverBackgroundColor: '#388e3c',
    },
  },
});

const App = () => (
  <ThemeProvider theme={customTheme}>
    <h1>Custom Theme Example</h1>
  </ThemeProvider>
);
```

## Extending the Default Theme

You can extend the default theme instead of creating one from scratch.

```tsx
import { defaultTheme, createTheme, ThemeProvider } from '@themakit/theme';

const extendedTheme = createTheme({
  ...defaultTheme,
  palette: {
    ...defaultTheme.palette,
    primary: '#2196f3',
  },
});

const App = () => (
  <ThemeProvider theme={extendedTheme}>
    <h1>Extended Theme Example</h1>
  </ThemeProvider>
);
```

## Customizing Components

You can customize individual components in your theme.

```tsx
const customTheme = createTheme({
  components: {
    Card: {
      backgroundColor: '#fff',
      borderRadius: '8px',
      boxShadow: '0 4px 6px rgba(0, 0, 0, 0.1)',
    },
  },
});
```

## Using Multiple Themes

You can use multiple themes in your application by wrapping different parts of your app with different `ThemeProvider` instances.

```tsx
const darkTheme = createTheme({
  palette: {
    background: '#212121',
    text: '#fff',
  },
});

const lightTheme = createTheme({
  palette: {
    background: '#f5f5f5',
    text: '#212121',
  },
});

const App = () => (
  <div>
    <ThemeProvider theme={darkTheme}>
      <div style={{ padding: '16px' }}>Dark Theme Section</div>
    </ThemeProvider>
    <ThemeProvider theme={lightTheme}>
      <div style={{ padding: '16px' }}>Light Theme Section</div>
    </ThemeProvider>
  </div>
);
```

## Next Steps

- Explore the [Theme API](theme-api.md) for more details on customizing themes.
- Check out the [Components](../../components/layout/container.md) section to see how themes are applied.