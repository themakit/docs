# Theming Overview

ThemaKit's theming system allows you to customize the appearance of all components to match your brand identity. The theming system is built to be flexible, type-safe, and easy to use.

## ThemeProvider

To apply a theme, wrap your application with the `ThemeProvider` component:

```tsx
import { ThemeProvider } from '@themakit/core';
import { defaultTheme } from '@themakit/theme';

function App() {
  return (
    <ThemeProvider theme={defaultTheme}>
    </ThemeProvider>
  );
}
```
## Theme Provider
A ThemaKit theme is an object with the following structure:
```tsx
const theme = {
  // Color palette
  colors: {
    primary: '#0066ff',
    secondary: '#6c757d',
    success: '#28a745',
    error: '#dc3545',
    warning: '#ffc107',
    info: '#17a2b8',
    // ... other colors
  },
  
  // Typography settings
  typography: {
    fontFamily: 'Inter, system-ui, sans-serif',
    fontSize: {
      xs: '0.75rem',
      sm: '0.875rem',
      md: '1rem',
      lg: '1.125rem',
      xl: '1.25rem',
      // ... other sizes
    },
    fontWeight: {
      regular: 400,
      medium: 500,
      bold: 700,
      // ... other weights
    },
    lineHeight: {
      tight: 1.25,
      normal: 1.5,
      loose: 1.75,
      // ... other line heights
    },
  },
  
  // Spacing system
  spacing: {
    xs: '0.25rem',
    sm: '0.5rem',
    md: '1rem',
    lg: '1.5rem',
    xl: '2rem',
    // ... other spacing values
  },
  
  // Border radius
  borderRadius: {
    sm: '0.125rem',
    md: '0.25rem',
    lg: '0.5rem',
    pill: '9999px',
  },
  
  // Shadows
  shadows: {
    sm: '0 1px 2px 0 rgba(0, 0, 0, 0.05)',
    md: '0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06)',
    lg: '0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05)',
    // ... other shadow values
  },
  
  // Component-specific styling
  components: {
    Button: {
      // ... button specific theme options
    },
    Card: {
      // ... card specific theme options
    },
    // ... other components
  }
};
```
## Using Built-in Themes
ThemaKit comes with several built-in themes:
```tsx
import { ThemeProvider } from '@themakit/core';
import { defaultTheme, darkTheme, systemTheme } from '@themakit/theme';

function App() {
  return (
    <ThemeProvider theme={darkTheme}>
      {/* Your application */}
    </ThemeProvider>
  );
}
```
## Creating Custom Themes
You can create custom themes by extending the default theme:
```tsx
import { createTheme } from '@themakit/theme';

const customTheme = createTheme({
  colors: {
    primary: '#ff4500', // Override primary color
    secondary: '#2e2e2e',
  },
  typography: {
    fontFamily: 'Poppins, sans-serif',
  },
  // ... other overrides
});
```
For more details on customizing specific aspects of the theme, see:

- Theme Provider
- [Custom Themes](../custom-themes)
- [Theme API](../theme-api)
- Dark Mode