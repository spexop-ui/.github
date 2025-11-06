# Spexop Design System

**Primitives-First Design System** built with TypeScript and React. Build modern web applications with production-ready components, a flexible theme system, and accessibility out of the box.

## ⚠️ Deprecation Notice

**Current package versions are deprecated.** We are pruning features to prepare for stable public release (v1.0.0). Please wait for the stable release or use the PRO version for advanced features.

**Status:** Maintenance mode - preparing for v1.0.0 stable release  
**Timeline:** Stable release coming after pruning  
**Alternative:** Use PRO version for advanced features  
**Updates:** See [GitHub](https://github.com/spexop-ui/spexop-packages) for progress

---

## ✨ Key Features

- **🎨 Design Tokens** - TypeScript-first token system with CSS variables
- **⚡ React Components** - ~60 production-ready, fully typed, tree-shakeable components
- **🎭 Theme System** - Basic presets and essential export formats
- **📦 Icon Library** - 281 optimized SVG icons with automatic tree-shaking
- **♿ Accessible** - WCAG 2.1 AA+ compliant components
- **🚀 High Performance** - Optimized bundles and rendering
- **💯 TypeScript** - 100% type coverage with full IntelliSense support
- **📱 Responsive** - Mobile-first design approach

---

## 📦 Packages

| Package | Description | Status |
|---------|-------------|--------|
| [`@spexop/react`](./packages/react) | React component library (~60 public tier components) | ⚠️ Deprecated - preparing for v1.0.0 |
| [`@spexop/theme`](./packages/theme) | Theme system (basic presets, essential formats) | ⚠️ Deprecated - preparing for v1.0.0 |
| [`@spexop/icons`](./packages/icons) | Icon library (281 icons) | ✅ Public |

**Note:** CLI and MCP tools are available in the PRO version only.

---

## 🚀 Quick Start

### Install Packages

```bash
npm install @spexop/react @spexop/theme @spexop/icons
```

### Basic Usage

```tsx
import { Button, Grid, Card, Icon } from '@spexop/react';
import { Home } from '@spexop/icons';
import '@spexop/theme/dist/css/tech.css';
import '@spexop/react/dist/index.css';

function App() {
  return (
    <Grid columns={12} gap={24}>
      <Card>
        <Icon name={Home} size={24} />
        <Button variant="primary">Get Started</Button>
      </Card>
    </Grid>
  );
}
```

### With Theme Configuration

```tsx
import { generateCSS, techPreset } from '@spexop/theme';
import { useThemeUtil } from '@spexop/react';
import { useEffect } from 'react';

function App() {
  useEffect(() => {
    const css = generateCSS(techPreset);
    const style = document.createElement('style');
    style.textContent = css;
    document.head.appendChild(style);
  }, []);

  const { resolvedMode, setMode } = useThemeUtil({ defaultMode: 'auto' });

  return <YourApp />;
}
```

---

## 🎨 Component Categories

**Primitives:** Grid, GridItem, Stack, Container, Spacer  
**Buttons:** Button, IconButton, ButtonGroup  
**Cards:** Card (with CardHeader, CardBody, CardFooter)  
**Forms:** TextInput, TextArea, Checkbox, RadioGroup, Select, Form, FormField, Toggle  
**Navigation:** Link, NavLink, Breadcrumb, Tabs, Pagination  
**Layout:** Section, Accordion, PageLayout, Footer  
**Overlays:** Modal, Tooltip, Popover  
**Display:** Avatar, Badge, Divider, Icon, Image, ThemeToggle  
**Feedback:** Alert, Spinner, Progress, Skeleton  
**Data:** Table  
**Typography:** Heading, Text, PageTitle  
**Animations:** FadeIn, Motion  
**Utilities:** ErrorBoundary

**Note:** Advanced components (Carousel, CodeBlock, DataTable, etc.) are available in the PRO version only.

---

## 📚 Resources

- **[Main Repository](https://github.com/spexop-ui/spexop-packages)** - Source code and documentation
- **[Component Documentation](./packages/react/README.md)** - Component API and examples
- **[Theme System Guide](./packages/theme/README.md)** - Theme configuration and usage
- **[Icons Catalog](./packages/icons/README.md)** - All 281 icons
- **[npm Packages](https://www.npmjs.com/org/spexop)** - Published packages

---

## 🎯 Design Philosophy

**The Spexop Way** - 7 Fundamental Principles:

1. **Primitives before patterns** - Master Grid, Stack, Container, Spacer first
2. **Borders before shadows** - Use strong 2-3px borders instead of heavy shadows
3. **Typography before decoration** - Font weight (600/700) for hierarchy, not lighter colors
4. **Tokens before magic numbers** - Use design tokens from @spexop/theme
5. **Composition before complexity** - Build up from simple parts
6. **Standards before frameworks** - Web platform fundamentals
7. **Accessibility before aesthetics** - WCAG AA+ compliance by default

---

## 🤝 Contributing

This workspace is in **maintenance mode** focused on stability, documentation, and bug fixes. New advanced features are developed in the PRO workspace.

**What we welcome:**
- Bug fixes
- Documentation improvements
- Accessibility enhancements
- Performance optimizations
- Community contributions

**What goes to PRO:**
- New advanced features
- New components
- Advanced utilities
- Experimental functionality

See [CONTRIBUTING.md](./CONTRIBUTING.md) for contribution guidelines.

---

## 📄 License

MIT © Spexop Team

---

## 🔗 Links

- **Website**: <https://spexop.com>
- **Documentation**: <https://github.com/spexop-ui/spexop-packages>
- **npm**: [@spexop/react](https://www.npmjs.com/package/@spexop/react), [@spexop/theme](https://www.npmjs.com/package/@spexop/theme), [@spexop/icons](https://www.npmjs.com/package/@spexop/icons)

---

<div align="center">

**Built with ❤️ by the Spexop Team**

[GitHub](https://github.com/spexop-ui/spexop-packages) • [npm](https://www.npmjs.com/org/spexop) • [Website](https://spexop.com)

</div>
