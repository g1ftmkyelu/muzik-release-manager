## Contributing

We welcome contributions to the Muzik Release Manager! Whether you're fixing bugs, improving documentation, or proposing new features, your help is appreciated.

### Getting Started

1. **Fork the Repository**
```bash
   git clone https://github.com/YOUR_USERNAME/muzik-release-manager.git
   cd muzik-release-manager
```

2. **Create a Branch**
```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
```

3. **Set Up Your Development Environment**
   Follow the [Getting Started](#getting-started) section to set up the project locally.

### Development Workflow

#### Code Style

- **TypeScript**: We use TypeScript for type safety across the entire stack.
- **Formatting**: Run `npm run format` before committing (if available).
- **Linting**: Ensure your code passes all linting checks with `npm run lint`.
- **Naming Conventions**:
  - Use `camelCase` for variables and functions
  - Use `PascalCase` for components, classes, and types
  - Use `UPPER_SNAKE_CASE` for constants and environment variables

#### Backend Development
```bash
cd server
npm run dev  # Start development server with hot reload
npm test     # Run tests
npm run build # Build TypeScript
```

**Backend Guidelines:**
- Place new routes in `src/routes/`
- Create services in `src/services/` for business logic
- Add controllers in `src/controllers/` for request handling
- Update Swagger documentation with JSDoc comments
- Write unit tests for new services and controllers
- Follow RESTful API conventions

#### Frontend Development
```bash
cd client
npm run dev   # Start development server
npm test      # Run tests
npm run build # Build for production
```

**Frontend Guidelines:**
- Create reusable components in `src/components/`
- Place page components in `src/pages/`
- Use React Context for global state management
- Follow the established component structure
- Ensure responsive design (mobile-first approach)
- Use Tailwind CSS utility classes consistently
- Write tests for complex components and logic

### Testing

- Write tests for all new features and bug fixes
- Ensure existing tests pass before submitting PR
- Aim for meaningful test coverage, not just high percentages

**Running Tests:**
```bash
# Backend tests
cd server && npm test

# Frontend tests
cd client && npm test

# Run all tests
npm test # (from root if script exists)
```

### Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, missing semi-colons, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

**Examples:**
```bash
feat(auth): add password reset functionality
fix(player): resolve audio playback issue on Safari
docs(readme): update installation instructions
refactor(api): simplify release approval logic
test(billing): add unit tests for payment integration
```

### Pull Request Process

1. **Update Documentation**
   - Update README.md if you've added new features
   - Add JSDoc comments for new functions/methods
   - Update API documentation if endpoints changed

2. **Test Your Changes**
```bash
   # Ensure all tests pass
   npm test
   
   # Test the full application flow
   ./start.sh native  # or start.bat native on Windows
```

3. **Create Pull Request**
   - Push your branch to your fork
   - Open a PR against the `main` branch
   - Fill out the PR template with:
     - Clear description of changes
     - Related issue numbers (if applicable)
     - Screenshots (for UI changes)
     - Testing steps

4. **PR Requirements**
   - All tests must pass
   - Code must be properly formatted and linted
   - No merge conflicts
   - At least one approving review (for collaborators)

### Reporting Bugs

When reporting bugs, please include:

1. **Description**: Clear and concise description of the bug
2. **Steps to Reproduce**: Detailed steps to reproduce the issue
3. **Expected Behavior**: What you expected to happen
4. **Actual Behavior**: What actually happened
5. **Environment**:
   - OS (e.g., Ubuntu 20.04, Windows 11, macOS 13)
   - Node.js version
   - Browser (if frontend issue)
6. **Screenshots/Logs**: If applicable
7. **Possible Solution**: If you have suggestions

**Bug Report Template:**
```markdown
**Bug Description**
A clear description of the bug.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '...'
3. See error

**Expected Behavior**
What should happen.

**Screenshots**
If applicable, add screenshots.

**Environment**
- OS: [e.g., Ubuntu 20.04]
- Node.js: [e.g., v18.16.0]
- Browser: [e.g., Chrome 120]

**Additional Context**
Any other relevant information.
```

### Suggesting Features

We love feature suggestions! When proposing new features:

1. **Search Existing Issues**: Check if the feature has been suggested before
2. **Provide Context**: Explain the problem you're trying to solve
3. **Describe the Solution**: Detail your proposed implementation
4. **Consider Alternatives**: Mention alternative approaches you've considered
5. **Additional Context**: Screenshots, mockups, or examples

**Feature Request Template:**
```markdown
**Feature Description**
Clear description of the feature.

**Problem Statement**
What problem does this solve?

**Proposed Solution**
How should this feature work?

**Alternatives Considered**
What other approaches did you consider?

**Additional Context**
Mockups, examples, or related features.
```

### Code Review Process

- All submissions require code review
- Maintainers will review PRs within 3-5 business days
- Address feedback and update your PR accordingly
- Once approved, a maintainer will merge your PR

### Development Best Practices

1. **Keep PRs Focused**: One feature or fix per PR
2. **Write Clear Code**: Prioritize readability over cleverness
3. **Document Complex Logic**: Add comments for non-obvious code
4. **Handle Errors Gracefully**: Provide meaningful error messages
5. **Secure by Default**: Never commit secrets or credentials
6. **Performance Matters**: Consider performance implications
7. **Accessibility First**: Ensure UI is accessible (WCAG guidelines)

### Database Changes

If your contribution involves database schema changes:

1. Document the changes in the PR description
2. Update `database/init.sql` accordingly
3. Provide migration scripts if needed
4. Test with a fresh database setup

### API Changes

For API endpoint changes:

1. Update Swagger documentation
2. Update relevant TypeScript types in `shared/`
3. Document breaking changes clearly
4. Consider backwards compatibility
5. Update API examples and documentation

### Questions or Need Help?

- **Documentation**: Check the README and inline code comments
- **Issues**: Search existing issues or create a new one
- **Discussions**: Use GitHub Discussions for general questions
- **Contact**: Reach out to maintainers at mkyelugift@gmail.com

### License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT License).

### Recognition

Contributors will be recognized in:
- GitHub contributors page
- Release notes for significant contributions
- CONTRIBUTORS.md file (if you'd like to be listed)

Thank you for contributing to Muzik Release Manager! 🎵
