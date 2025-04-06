# Installation

## Package Structure

ThemaKit is distributed as a collection of packages under the `@themakit` scope. This modular approach allows you to install only the components you need.

### Core Packages

```bash
# Install the core package (required)
npm install @themakit/core

# Install the theme package (recommended)
npm install @themakit/theme
```
## Component Packages
Install only the component packages you need:
```bash
# Layout components
npm install @themakit/layout

# Input components
npm install @themakit/button @themakit/input @themakit/select @themakit/checkbox

# Display components
npm install @themakit/card @themakit/modal @themakit/alert @themakit/toast
```
## All-in-one Package
If you prefer to install everything at once:
```bash
npm install @themakit/core @themakit/theme @themakit/components
```
## Peer Dependencies
ThemaKit requires the following peer dependencies:
```bash
npm install react react-dom
```
ThemaKit supports React 18 and above.
## Typescript
ThemaKit is built with TypeScript and includes type definitions for all components. To get the best development experience, we recommend using TypeScript in your project.
```bash
npm install typescript @types/react @types/react-dom --save-dev
```


## Next Steps
After installation, check out our [Quick Start](../quick-start) guide to begin building with ThemaKit.