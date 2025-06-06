# M-WC-Figlet Web Component

A modern web component that generates ASCII art text using the figlet library. This component is built with Lit and follows the [open-wc](https://github.com/open-wc/open-wc) recommendations.

## Features

- 📝 Convert text to ASCII art with various fonts
- 🎨 Multiple font options (Standard, 3D Diagonal, Ghost, Graffiti, etc.)
- ⚡ Built with Lit for high performance
- 🔧 Follows open-wc best practices
- 📱 Responsive design with Materialize CSS in demo
- 🐳 Docker support for easy deployment

## Project Structure

```
├── m-wc-figlet/              # Main web component package
│   ├── src/
│   │   └── MWcFiglet.js      # Main component implementation
│   ├── demo/                 # Live demo application
│   │   ├── index.html
│   │   ├── main.js
│   │   └── styles.css
│   ├── stories/              # Storybook stories
│   └── package.json
├── Dockerfile                # Docker configuration
└── README.md
```

## Quick Start

### Using Docker

```bash
# Clone the repository
git clone <your-repo-url>
cd m-gwc-figlet

# Build and run with Docker
docker build -t m-wc-figlet .
docker run -p 8000:8000 m-wc-figlet
```

Visit `http://localhost:8000` to see the demo.

### Local Development

```bash
# Navigate to the component directory
cd m-wc-figlet

# Install dependencies
npm install

# Start development server
npm start
```

This will open the demo at `http://localhost:8000/demo/`.

## Usage

### As a Web Component

```html
<script type="module">
  import 'm-wc-figlet/m-wc-figlet.js';
</script>

<m-wc-figlet text="Hello World" font="Standard"></m-wc-figlet>
```

### Programmatically

```javascript
import { MWcFiglet } from 'm-wc-figlet';

const figletElement = new MWcFiglet();
figletElement.text = 'Your Text Here';
figletElement.font = 'Ghost';
document.body.appendChild(figletElement);
```

## Properties

| Property | Type | Default | Description |
|----------|------|---------|-------------|
| `text` | String | - | The text to convert to ASCII art |
| `font` | String | - | The figlet font to use |

## Available Fonts

- Standard
- 3D Diagonal
- Dancing Font
- Ghost
- Graffiti
- Patorjk's Cheese
- Pagga
- Pawp

## Development Scripts

```bash
# Start development server
npm start

# Lint code
npm run lint

# Format code
npm run format

# Run Storybook
npm run storybook

# Build Storybook
npm run storybook:build

# Analyze custom elements
npm run analyze
```

## Demo

The project includes a fully functional demo with:
- Real-time text input
- Font selection dropdown
- Live preview of ASCII art output
- Responsive design using Materialize CSS

## Docker Deployment

The project includes a Dockerfile for easy deployment:

```bash
docker build -t m-wc-figlet .
docker run -p 8000:8000 m-wc-figlet
```

## Technologies Used

- **Lit** - Fast, lightweight web components
- **Figlet** - ASCII art text generation
- **Materialize CSS** - UI framework for demo
- **Web Dev Server** - Development server
- **Storybook** - Component documentation
- **ESLint & Prettier** - Code quality tools

## Browser Support

This component uses modern web standards and supports all modern browsers that support:
- Custom Elements
- ES6 Modules
- CSS Custom Properties

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Make your changes
4. Run tests and linting: `npm run lint`
5. Commit your changes: `git commit -am 'Add new feature'`
6. Push to the branch: `git push origin feature/new-feature`
7. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](m-wc-figlet/LICENSE) file for details.

## Acknowledgments

- Built with [open-wc](https://github.com/open-wc/open-wc) recommendations
- Uses [figlet](https://www.npmjs.com/package/figlet) for ASCII art generation
- Demo styled with [Materialize CSS](https://materializecss.com/)
