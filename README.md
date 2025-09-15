# Python Project Template

A modern Python project template with development container support, package management via UV, and integrated tooling for code quality and testing.

## Features

- 🐳 **Dev Container**: Pre-configured development environment with Python 3.11
- 📦 **UV Package Manager**: Fast Python package management and dependency resolution
- 🛠️ **Makefile**: Convenient commands for common development tasks
- 🔍 **Type Checking**: Strict type checking with Pyright
- 🧪 **Testing**: Testing framework with pytest and pytest-mock
- 📓 **Jupyter Support**: Integrated Jupyter notebook support
- 🌍 **Environment Management**: Environment variable template for Azure OpenAI
- ✨ **Code Formatting**: Code formatting with Ruff

## Development Setup

This project uses a dev container for consistent development environment setup.

### Prerequisites

- Docker
- Visual Studio Code with Dev Containers extension

### Getting Started

1. Open this project in VS Code
2. Copy `.env.example` to `.env` and configure your environment variables
3. When prompted, click "Reopen in Container" or use the Command Palette: `Dev Containers: Reopen in Container`
4. Wait for the container to build and start (this runs `make setup` automatically)

### Package Management

This project uses [uv](https://github.com/astral-sh/uv) as the package manager with Make commands for convenience.

#### Quick Start

```bash
# Set up the environment (installs uv and dependencies)
make setup

# Install/update dependencies
make install

# Clean environment
make clean
```

#### Adding New Dependencies

Edit `pyproject.toml` to add dependencies, then run:

```bash
make install
```

### Development Commands

The project includes several Make targets for common development tasks:

```bash
# Install dependencies
make install

# Run tests
make test

# Format code
make format  # or make fmt

# Type check code
make lint

# Clean cache files
make clear-cache

# Clean environment
make clean

# Show all available commands
make help
```

### Code Quality

The project is configured with several code quality tools:

- **Ruff**: Fast Python formatter
- **Pyright**: Strict type checking
- **pytest**: Testing framework with mocking support

### Environment Variables

The project includes support for environment variables, particularly for Azure OpenAI integration. Copy `.env.example` to `.env` and configure as needed:

```bash
cp .env.example .env
```

## Project Structure

```text
project/
├── .devcontainer/          # Dev container configuration
│   └── devcontainer.json   # VS Code dev container settings
├── src/                    # Source code directory
├── tests/                  # Test files directory
├── .env.example            # Environment variables template
├── .env                    # Your environment variables (create from .env.example)
├── .gitignore              # Git ignore patterns
├── Makefile                # Development commands
├── pyproject.toml          # Project configuration and dependencies
├── uv.lock                 # Locked dependencies
└── README.md               # This file
```

### Getting Started with Your Code

The template includes `src/` and `tests/` directories ready for your code:

```bash
# Add your modules to src/
touch src/your_module.py

# Add your tests to tests/
touch tests/test_your_module.py

# Run tests
make test
```
