<!-- markdownlint-disable MD013 MD033 MD041 -->
<div align="center">
<h1>
Django-Tailwind-DaisyUI Template
</h1>
</div>

<p align="center">
<a href="https://www.djangoproject.com/"><img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" alt="Django badge" /></a>
<a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white" alt="Tailwind CSS badge" /></a>
<a href="https://daisyui.com/"><img src="https://img.shields.io/badge/DaisyUI-5A0EF8?style=flat-square&logo=daisyui&logoColor=white" alt="DaisyUI badge" /></a>
<a href="https://python.org/"><img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python badge" /></a>
<a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js badge" /></a>
</p>

[Overview](#overview)&nbsp;•
[Features](#features)&nbsp;•
[Installation](#installation)&nbsp;•
[Usage](#usage)&nbsp;•
[Configuration](#configuration)&nbsp;•
[Contributing](#contributing)&nbsp;•
[License](#license)

## Overview <a name="overview"></a>

A modern Django project template with Tailwind CSS and DaisyUI integration, providing a beautiful, responsive UI framework with minimal effort. This template combines the power of Django's backend capabilities with the utility-first approach of Tailwind CSS and the component-rich features of DaisyUI.

Perfect for quickly bootstrapping web applications with a professional look and feel, while maintaining complete customization control.

## Features <a name="features"></a>

- **Django Integration**: Full Django framework with best practices
- **Tailwind CSS**: Utility-first CSS framework for rapid UI development
- **DaisyUI Components**: Pre-designed beautiful components built on Tailwind CSS
- **Theme Support**: Multiple themes with easy switching capability
- **Responsive Design**: Mobile-first responsive layouts
- **Environment Configuration**: Environment variables support via dotenv
- **Development Workflow**: Hot-reloading CSS changes during development
- **Production Ready**: Optimized builds for production deployment

## Installation <a name="installation"></a>

1. Clone this repository:
   ```bash
   git clone <your-repository-url>
   cd <project-directory>
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the project root:
   ```
   # Django Tailwind Configuration
   NPM_BIN_PATH=C:\\Program Files\\nodejs\\npm.cmd
   # For macOS/Linux
   # NPM_BIN_PATH=/usr/bin/npm
   ```

5. Install Tailwind CSS dependencies:
   ```bash
   cd theme
   npm install
   cd ..
   ```

## Usage <a name="usage"></a>

1. Start the Tailwind CSS watcher to compile CSS automatically:
   ```bash
   python manage.py tailwind start
   ```

2. In another terminal, start the Django development server:
   ```bash
   python manage.py runserver
   ```

3. Visit http://localhost:8000 in your browser to see the application.

## Configuration <a name="configuration"></a>

### Tailwind CSS Configuration

The Tailwind CSS configuration is located in `theme/static_src/tailwind.config.js`. You can customize themes, colors, and plugins here.

```javascript
module.exports = {
    // ... other configurations
    plugins: [
        // ... other plugins
        require('daisyui'),
    ],
    daisyui: {
        themes: ["light", "dark", "cupcake"],
    },
}
```

### Django Settings

Key settings for the Django-Tailwind integration:

```python
# settings.py
INSTALLED_APPS = [
    # ... other apps
    'tailwind',
    'theme',
]

TAILWIND_APP_NAME = 'theme'
NPM_BIN_PATH = os.getenv('NPM_BIN_PATH')  # Loaded from .env file
```

### Adding More DaisyUI Themes

To add more themes, update the `daisyui.themes` array in `tailwind.config.js`:

```javascript
daisyui: {
    themes: ["light", "dark", "cupcake", "corporate", "synthwave"],
},
```

## Contributing <a name="contributing"></a>

Contributions are welcome! Here's how you can contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

## License <a name="license"></a>

This project is dual-licensed under both the MIT License and the GNU General Public License v3.0 (GPL-3.0).

### MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### GNU GPL v3.0

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>. 