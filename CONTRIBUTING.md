# Contributing to Exact Word Counter

First off, thank you for considering contributing to Exact Word Counter! It's people like you that make this tool better for everyone.

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

### Our Standards

- **Be respectful**: Treat everyone with respect and kindness
- **Be constructive**: Provide helpful feedback and suggestions
- **Be collaborative**: Work together towards common goals
- **Be inclusive**: Welcome newcomers and diverse perspectives

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

**Bug Report Template:**
```markdown
**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Type '....'
4. See error

**Expected behavior**
A clear description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Environment:**
 - OS: [e.g. Windows 11, macOS 13, Ubuntu 22.04]
 - Browser: [e.g. Chrome 120, Firefox 121]
 - Version: [e.g. 1.0.0]

**Additional context**
Add any other context about the problem here.
```

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

- **Clear title**: Use a descriptive title
- **Use case**: Explain why this enhancement would be useful
- **Detailed description**: Provide a step-by-step description
- **Examples**: Include examples of how the feature would work
- **Alternatives**: List any alternatives you've considered

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** following our coding standards
3. **Test thoroughly** to ensure nothing breaks
4. **Update documentation** if you're changing functionality
5. **Write a good commit message** following our guidelines
6. **Submit a pull request** with a clear description

## Development Process

### Getting Started

1. Fork and clone the repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/Word_Counter.git
   cd Word_Counter
   ```

2. Create a branch for your changes:
   ```bash
   git checkout -b feature/my-new-feature
   # or
   git checkout -b fix/bug-description
   ```

3. Make your changes and test locally:
   ```bash
   # Open index.html in your browser
   # Or serve with a local server
   python3 -m http.server 8000
   ```

### Coding Standards

#### HTML
- Use semantic HTML5 elements
- Include ARIA labels for accessibility
- Maintain proper indentation (4 spaces)
- Keep structure clean and organized

#### CSS
- Use CSS custom properties for theming
- Follow BEM-like naming conventions
- Ensure responsive design
- Support both light and dark modes
- Keep specificity low

#### JavaScript
- Write ES6+ modern JavaScript
- Use `const` and `let`, never `var`
- Add JSDoc comments for functions
- Follow functional programming patterns where possible
- Handle errors gracefully
- Test in multiple browsers

#### Example JavaScript Style:
```javascript
/**
 * Calculate the average word length in an array of words
 * @param {string[]} words - Array of words to analyze
 * @returns {string} Average word length with 1 decimal place
 */
function calculateAverageWordLength(words) {
    if (words.length === 0) return '0.0';
    const totalLength = words.reduce((sum, word) => sum + word.length, 0);
    return (totalLength / words.length).toFixed(1);
}
```

### Commit Message Guidelines

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that don't affect code meaning (formatting, etc.)
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `perf`: Performance improvement
- `test`: Adding missing tests
- `chore`: Changes to build process or auxiliary tools

**Examples:**
```
feat(stats): add paragraph count statistic

Add a new paragraph count feature that accurately counts paragraphs
separated by blank lines. Updates the stats grid layout to accommodate
the new metric.

Closes #123
```

```
fix(dark-mode): correct text color in input field

The input field text was invisible in dark mode. Updated the CSS
to use the correct text color variable.
```

### Testing Checklist

Before submitting a pull request, ensure:

- [ ] Code runs without errors in Chrome, Firefox, Safari, Edge
- [ ] All features work as expected
- [ ] Dark mode displays correctly
- [ ] Responsive design works on mobile/tablet/desktop
- [ ] Keyboard shortcuts function properly
- [ ] Screen reader announcements work
- [ ] LocalStorage saves/loads correctly
- [ ] PWA installation works
- [ ] Service worker caches correctly
- [ ] No console errors or warnings

### Pull Request Process

1. **Update the README.md** with details of changes if applicable
2. **Update the CHANGELOG.md** with your changes
3. **Ensure your code follows** the style guidelines
4. **Test your changes** thoroughly
5. **Create a pull request** with a clear title and description

**Pull Request Template:**
```markdown
## Description
Brief description of what this PR does

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## How Has This Been Tested?
Describe the tests you ran and browsers you tested in.

## Checklist
- [ ] My code follows the style guidelines
- [ ] I have performed a self-review
- [ ] I have commented my code where necessary
- [ ] I have updated the documentation
- [ ] My changes generate no new warnings
- [ ] I have tested on multiple browsers
```

## Recognition

Contributors will be acknowledged in:
- Project README
- Release notes
- Git commit history

Thank you for your contributions!

## Questions?

Don't hesitate to ask questions by:
- Opening a GitHub Discussion
- Commenting on relevant issues
- Reaching out to maintainers

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
