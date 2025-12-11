# Contributing to go-ssh

Thank you for your interest in contributing to go-ssh! This document provides guidelines and instructions for contributing.

## Code of Conduct

Be respectful and inclusive. We aim to create a welcoming environment for all contributors.

## How to Contribute

### Reporting Bugs

1. Check if the bug has already been reported in [Issues](https://github.com/mr-kaynak/go-ssh/issues)
2. If not, create a new issue with:
   - Clear title and description
   - Steps to reproduce
   - Expected vs actual behavior
   - System information (OS, Go version, etc.)

### Suggesting Features

1. Check existing issues and pull requests
2. Create an issue describing:
   - The problem you're trying to solve
   - Your proposed solution
   - Any alternative approaches considered

### Pull Requests

1. Fork the repository
2. Create a feature branch from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make your changes:
   - Follow the existing code style
   - Add tests for new functionality
   - Update documentation as needed
   - Ensure tests pass: `make test`

4. Commit your changes:
   ```bash
   git commit -m "feat: add amazing feature"
   ```

   Follow [Conventional Commits](https://www.conventionalcommits.org/):
   - `feat:` for new features
   - `fix:` for bug fixes
   - `docs:` for documentation
   - `test:` for tests
   - `refactor:` for refactoring
   - `chore:` for maintenance

5. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```

6. Create a Pull Request:
   - Provide a clear description
   - Reference any related issues
   - Ensure CI passes

## Development Setup

### Prerequisites

- Go 1.21 or later
- Make (optional but recommended)
- Git

### Getting Started

1. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/go-ssh.git
   cd go-ssh
   ```

2. Install dependencies:
   ```bash
   make deps
   ```

3. Build the project:
   ```bash
   make build
   ```

4. Run in development mode:
   ```bash
   make dev
   ```

### Running Tests

```bash
# Run all tests
make test

# Run tests with verbose output
go test -v ./...

# Run tests for a specific package
go test -v ./internal/ssh/
```

### Code Style

- Run `make fmt` to format code
- Run `make lint` to check for issues
- Follow standard Go conventions
- Keep functions small and focused
- Write clear comments for exported functions

### Project Structure

- `cmd/go-ssh/` - Main entry point
- `internal/app/` - Application logic
- `internal/ssh/` - SSH key operations
- `internal/tui/` - Terminal UI components
- `internal/clipboard/` - Clipboard operations

### Testing Guidelines

- Write tests for new functionality
- Aim for >80% code coverage
- Use table-driven tests where appropriate
- Mock external dependencies
- Test edge cases and error conditions

## Release Process

Releases are automated via GitHub Actions:

1. Update version in relevant files
2. Create a git tag:
   ```bash
   git tag v0.1.0
   git push origin v0.1.0
   ```
3. GitHub Actions will:
   - Run tests
   - Build binaries for all platforms
   - Create GitHub release
   - Update Homebrew formula

## Questions?

Feel free to open an issue for any questions or clarifications needed.

Thank you for contributing! 🎉