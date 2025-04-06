# Dark Mode

ThemaKit supports dark mode, allowing you to create a visually appealing experience for users in low-light environments.

## Enabling Dark Mode

You can enable dark mode by creating a custom theme with a dark color palette.

```tsx
import { createTheme, ThemeProvider } from '@themakit/theme';

const darkTheme = createTheme({
  palette: {
    background: '#121212',
    text: '#ffffff',
    primary: '#bb86fc',
    accent: '#03dac6',
  },
  components: {
    Button: {
      backgroundColor: '#bb86fc',
      color: '#ffffff',
      hoverBackgroundColor: '#3700b3',
    },
  },
});

const App = () => (
  <ThemeProvider theme={darkTheme}>
    <h1>Dark Mode Example</h1>
  </ThemeProvider>
);
```

## Switching Between Light and Dark Mode

You can dynamically switch between light and dark themes based on user preferences or a toggle.

```tsx
import React, { useState } from 'react';
import { createTheme, ThemeProvider } from '@themakit/theme';

const lightTheme = createTheme({
  palette: {
    background: '#ffffff',
    text: '#000000',
    primary: '#4caf50',
    accent: '#ff5722',
  },
});

const darkTheme = createTheme({
  palette: {
    background: '#121212',
    text: '#ffffff',
    primary: '#bb86fc',
    accent: '#03dac6',
  },
});

const App = () => {
  const [isDarkMode, setIsDarkMode] = useState(false);

  return (
    <ThemeProvider theme={isDarkMode ? darkTheme : lightTheme}>
      <button onClick={() => setIsDarkMode(!isDarkMode)}>
        Toggle Dark Mode
      </button>
      <h1>{isDarkMode ? 'Dark Mode' : 'Light Mode'}</h1>
    </ThemeProvider>
  );
};
```

## Using System Preferences

You can detect the user's system preference for dark mode using the `window.matchMedia` API.

```tsx
import React, { useEffect, useState } from 'react';
import { createTheme, ThemeProvider } from '@themakit/theme';

const lightTheme = createTheme({
  palette: {
    background: '#ffffff',
    text: '#000000',
    primary: '#4caf50',
    accent: '#ff5722',
  },
});

const darkTheme = createTheme({
  palette: {
    background: '#121212',
    text: '#ffffff',
    primary: '#bb86fc',
    accent: '#03dac6',
  },
});

const App = () => {
  const [isDarkMode, setIsDarkMode] = useState(
    window.matchMedia('(prefers-color-scheme: dark)').matches
  );

  useEffect(() => {
    const mediaQuery = window.matchMedia('(prefers-color-scheme: dark)');
    const handleChange = () => setIsDarkMode(mediaQuery.matches);
    mediaQuery.addEventListener('change', handleChange);
    return () => mediaQuery.removeEventListener('change', handleChange);
  }, []);

  return (
    <ThemeProvider theme={isDarkMode ? darkTheme : lightTheme}>
      <h1>{isDarkMode ? 'Dark Mode' : 'Light Mode'}</h1>
    </ThemeProvider>
  );
};
```

## Accessibility

- Ensure sufficient contrast between text and background colors in dark mode.
- Test your application in both light and dark modes to ensure a consistent user experience.

## Next Steps

- Learn more about [Custom Themes](custom-themes.md) to further customize your dark mode.
- Explore the [Theme API](theme-api.md) for advanced theming options.