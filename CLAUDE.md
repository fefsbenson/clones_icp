# CLAUDE.md

**Last Updated:** 2025-11-14
**Repository:** clones_icp (Processo de clonagem de públicos)

This document provides comprehensive guidance for AI assistants working with this codebase.

---

## Table of Contents

1. [Repository Overview](#repository-overview)
2. [Codebase Structure](#codebase-structure)
3. [Development Workflow](#development-workflow)
4. [Key Conventions](#key-conventions)
5. [Technology Stack](#technology-stack)
6. [Testing Guidelines](#testing-guidelines)
7. [Common Tasks](#common-tasks)
8. [Important Notes](#important-notes)

---

## Repository Overview

**Purpose:** Public cloning process (Processo de clonagem de públicos)

**Repository State:** This is a new repository currently in its initial setup phase. The primary language appears to be Portuguese (Brazilian).

**Main Branch:** Not yet established (currently working on feature branches)

**Owner:** fefsbenson

---

## Codebase Structure

```
clones_icp/
├── .git/                 # Git version control
├── README.md             # Project overview (Portuguese)
└── CLAUDE.md            # This file - AI assistant guide
```

### Expected Structure (To Be Implemented)

As this project develops, the following structure is recommended:

```
clones_icp/
├── src/                  # Source code
│   ├── main/            # Main application code
│   ├── utils/           # Utility functions
│   └── config/          # Configuration files
├── tests/               # Test files
├── docs/                # Documentation
├── scripts/             # Build and deployment scripts
├── .gitignore           # Git ignore rules
├── package.json         # Project dependencies (if Node.js)
├── requirements.txt     # Python dependencies (if Python)
└── README.md            # Project documentation
```

---

## Development Workflow

### Branch Strategy

- **Feature Branches:** Use `claude/claude-md-*` naming convention for AI-assisted development
- **Commit Messages:** Write clear, descriptive commits in English or Portuguese
- **Push Strategy:** Always use `git push -u origin <branch-name>`

### Git Operations

**Important:** All feature branches must start with `claude/` and match the session ID to avoid 403 errors.

#### Commit Workflow

```bash
# Check status
git status

# Stage changes
git add <files>

# Commit with descriptive message
git commit -m "feat: description of changes"

# Push to remote
git push -u origin <branch-name>
```

#### Common Git Commands

```bash
# Create new branch
git checkout -b claude/<feature-name>

# Fetch specific branch
git fetch origin <branch-name>

# Pull latest changes
git pull origin <branch-name>

# View commit history
git log --oneline --graph --all
```

### Retry Logic for Network Operations

For git push/fetch/pull operations, retry up to 4 times with exponential backoff (2s, 4s, 8s, 16s) if network failures occur.

---

## Key Conventions

### Language

- **Code Comments:** Portuguese (primary) or English
- **Documentation:** Portuguese (align with README.md)
- **Variable Naming:** Use clear, descriptive names in English or Portuguese
- **Function Names:** camelCase or snake_case (depending on technology stack)

### Code Style

**To Be Defined** - Establish conventions as the codebase develops:

- Indentation: 2 or 4 spaces (to be determined by technology choice)
- Line length: 80-120 characters
- File organization: Group related functionality
- Import ordering: Standard library → Third-party → Local imports

### Security Best Practices

1. **Never commit sensitive data:**
   - API keys
   - Passwords
   - Tokens
   - Database credentials
   - .env files with secrets

2. **Input validation:**
   - Validate all user inputs
   - Sanitize data before processing
   - Use parameterized queries for database operations

3. **Error handling:**
   - Never expose stack traces to end users
   - Log errors appropriately
   - Use try-catch blocks for error-prone operations

4. **OWASP Top 10 Prevention:**
   - Prevent SQL injection
   - Prevent XSS attacks
   - Prevent command injection
   - Use HTTPS for all communications
   - Implement proper authentication and authorization

---

## Technology Stack

**To Be Determined** - The technology stack will be defined as development progresses.

### Potential Technologies

Based on the project name and purpose, consider:

- **Backend:** Node.js, Python (Django/Flask), or Java
- **Database:** PostgreSQL, MongoDB, or MySQL
- **API:** REST or GraphQL
- **Testing:** Jest, PyTest, or JUnit
- **CI/CD:** GitHub Actions, GitLab CI, or Jenkins

---

## Testing Guidelines

### Test Structure (To Be Implemented)

```
tests/
├── unit/           # Unit tests for individual functions
├── integration/    # Integration tests for modules
└── e2e/           # End-to-end tests
```

### Testing Best Practices

1. **Write tests for:**
   - Core business logic
   - Edge cases
   - Error handling
   - Security-critical functions

2. **Test naming:**
   - Use descriptive names: `test_should_clone_public_when_valid_input`
   - Follow AAA pattern: Arrange, Act, Assert

3. **Test coverage:**
   - Aim for >80% code coverage
   - Focus on critical paths first

4. **Running tests:**
   ```bash
   # To be defined based on technology stack
   # npm test (Node.js)
   # pytest (Python)
   # mvn test (Java)
   ```

---

## Common Tasks

### For AI Assistants

When working on this codebase, follow these guidelines:

#### 1. Starting a New Task

```markdown
1. Read relevant files to understand context
2. Create a todo list using TodoWrite tool
3. Plan the implementation approach
4. Execute changes incrementally
5. Test changes
6. Commit and push
```

#### 2. Adding New Features

```markdown
1. Understand the feature requirements
2. Check existing code for similar patterns
3. Design the implementation
4. Write code following project conventions
5. Add tests for the new feature
6. Update documentation if needed
7. Commit with clear message: "feat: <description>"
```

#### 3. Fixing Bugs

```markdown
1. Reproduce the bug
2. Identify root cause
3. Write a test that fails (demonstrates the bug)
4. Fix the bug
5. Verify the test passes
6. Commit with message: "fix: <description>"
```

#### 4. Refactoring

```markdown
1. Ensure tests exist for the code being refactored
2. Make changes incrementally
3. Run tests after each change
4. Commit with message: "refactor: <description>"
```

### File Operations

- **Reading:** Use `Read` tool for specific files
- **Editing:** Use `Edit` tool for modifications
- **Creating:** Use `Write` tool (only when necessary)
- **Searching:** Use `Grep` for content, `Glob` for file patterns

### Never Use Bash For

- Reading files (use `Read` tool)
- Editing files (use `Edit` tool)
- Creating files (use `Write` tool)
- File searching (use `Grep` or `Glob` tools)
- Communication with users (output text directly)

---

## Important Notes

### For AI Assistants

1. **Always use TodoWrite** for complex tasks to track progress
2. **Security first:** Never introduce vulnerabilities
3. **Test before committing:** Ensure changes don't break existing functionality
4. **Clear commits:** Write descriptive commit messages
5. **Ask when unclear:** If requirements are ambiguous, ask the user
6. **Incremental changes:** Make small, focused commits
7. **Documentation:** Update docs when making significant changes

### Project-Specific Guidelines

**ICP (Internet Computer Protocol) Context:**

This project appears to be related to "cloning" processes, possibly for:
- Data replication
- Public dataset management
- Distributed system synchronization
- Blockchain/ICP canister deployment

**As the project develops, update this section with:**
- Specific ICP integration details
- Canister deployment procedures
- Identity and authentication patterns
- Network configuration

### Configuration Files to Create

As the project grows, consider adding:

```bash
.gitignore          # Ignore build artifacts, dependencies, secrets
.editorconfig       # Consistent editor settings
.prettierrc         # Code formatting rules
eslint.config.js    # Linting rules (if JavaScript/TypeScript)
pytest.ini          # Test configuration (if Python)
Dockerfile          # Container configuration
docker-compose.yml  # Multi-container setup
CI/CD config        # GitHub Actions, GitLab CI, etc.
```

---

## Changelog

### 2025-11-14
- Initial CLAUDE.md creation
- Repository analysis completed
- Development guidelines established
- Structure recommendations provided

---

## Questions or Issues?

When encountering issues:

1. Check this CLAUDE.md file first
2. Review existing code patterns
3. Consult project README.md
4. Ask the repository owner for clarification

---

**Note to Future AI Assistants:**

This document should be updated as the project evolves. When you make significant changes to:
- Project structure
- Technology stack
- Development workflows
- Testing strategies
- Coding conventions

Please update the relevant sections in this file and note the changes in the Changelog section.

---

*This file was generated to assist AI assistants in understanding and working with the clones_icp codebase efficiently and following best practices.*
