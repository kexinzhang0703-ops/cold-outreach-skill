# Contributing to Cold Outreach Skill

Thank you for your interest in contributing! This document provides guidelines for contributing to the Cold Outreach Skill for Claude.

## 🤝 How to Contribute

### Types of Contributions

We welcome:

1. **New Templates**: Additional message templates for specific scenarios
2. **Template Improvements**: Better wording, structure, or examples
3. **Bug Fixes**: Corrections to existing templates or documentation
4. **Documentation**: Clarifications, examples, or translations
5. **Feature Requests**: New functionality or use cases

### Before You Start

- Check existing [Issues](https://github.com/YOUR_USERNAME/cold-outreach-skill/issues) to avoid duplicates
- For major changes, open an issue first to discuss
- Review the [SKILL.md](SKILL.md) to understand the current workflow

## 📝 Contribution Guidelines

### Adding New Templates

When adding a new template to `references/templates.md`:

1. **Follow the existing structure**:
   ```markdown
   ### Template Name
   
   Message template here...
   
   **When to use**: Specific scenario description
   
   **Key elements**:
   - Element 1
   - Element 2
   ```

2. **Include**:
   - Clear template with [placeholders]
   - When to use this template
   - Customization points
   - Character count (for LinkedIn messages)
   - Example (optional but helpful)

3. **Test the template**:
   - Does it fit LinkedIn's 300-character limit (if applicable)?
   - Is it professional yet warm?
   - Does it include a clear ask?
   - Can it be easily customized?

### Improving Existing Templates

When modifying templates:

1. **Explain the improvement** in your pull request
2. **Provide before/after examples**
3. **Consider character count** (for LinkedIn templates)
4. **Maintain professional tone**

### Documentation Changes

- Use clear, concise language
- Include examples where helpful
- Update table of contents if adding sections
- Check for spelling and grammar

## 🔧 Technical Guidelines

### File Structure

```
cold-outreach-skill/
├── SKILL.md                    # Main skill instructions
├── README.md                   # Overview and documentation
├── CONTRIBUTING.md             # This file
├── LICENSE                     # MIT License
└── references/
    ├── templates.md            # All message templates
    ├── coffee-chat-guide.md    # Coffee chat SOP
    └── recruiter-strategy.md   # Recruiter outreach guide
```

### Naming Conventions

- Use lowercase with hyphens for files: `new-template-name.md`
- Use clear, descriptive names
- Keep filenames under 50 characters

### Markdown Style

- Use `##` for main sections, `###` for subsections
- Use code blocks with triple backticks for templates
- Use **bold** for emphasis, *italics* for definitions
- Include blank lines between sections

## 🚀 Submission Process

### 1. Fork the Repository

```bash
git clone https://github.com/YOUR_USERNAME/cold-outreach-skill.git
cd cold-outreach-skill
```

### 2. Create a Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix
```

### 3. Make Your Changes

- Edit relevant files
- Test templates if applicable
- Update documentation

### 4. Commit Your Changes

```bash
git add .
git commit -m "Add: brief description of changes"
```

**Commit message format**:
- `Add: [description]` for new features
- `Fix: [description]` for bug fixes
- `Update: [description]` for improvements
- `Docs: [description]` for documentation

### 5. Push and Create Pull Request

```bash
git push origin feature/your-feature-name
```

Then create a pull request on GitHub.

## ✅ Pull Request Checklist

Before submitting:

- [ ] My code follows the existing style
- [ ] I have tested my templates (if applicable)
- [ ] Character counts are correct for LinkedIn templates
- [ ] Documentation is updated if needed
- [ ] Commit messages are clear
- [ ] No unnecessary files are included

## 🎯 Quality Standards

### For Templates

- **Professional tone**: Not too formal, not too casual
- **Specific ask**: Clear, time-bounded requests
- **Personalization**: Include [placeholder] points
- **Concise**: Remove filler words
- **Authentic**: Sound genuine, not robotic

### For Documentation

- **Clear**: Easy to understand
- **Complete**: No missing information
- **Accurate**: No misleading content
- **Well-formatted**: Proper markdown

## 💡 Ideas for Contributions

Not sure what to contribute? Here are some ideas:

1. **Industry-specific templates**:
   - Tech/software engineering
   - Finance/banking
   - Consulting
   - Healthcare
   - Marketing

2. **Special scenarios**:
   - Reaching out to speakers after conferences
   - Connecting with podcast hosts
   - Academic/research networking
   - Startup founder outreach

3. **Internationalization**:
   - Templates for different cultures
   - Translations (Mandarin, Spanish, etc.)
   - Regional etiquette notes

4. **Analytics**:
   - Response rate tracking
   - A/B testing frameworks
   - Success metrics

## 🐛 Reporting Bugs

If you find a bug:

1. **Check existing issues** first
2. **Create a new issue** with:
   - Clear title
   - Description of the problem
   - Steps to reproduce
   - Expected vs. actual behavior
   - Screenshots if applicable

## 📮 Questions?

- Open an issue for questions
- Tag with `question` label
- Be specific about what you need help with

## 📜 Code of Conduct

### Our Standards

- Be respectful and inclusive
- Welcome diverse perspectives
- Give and receive constructive feedback
- Focus on what's best for the community

### Unacceptable Behavior

- Harassment or discrimination
- Trolling or insulting comments
- Publishing others' private information
- Unprofessional conduct

## 🙏 Recognition

Contributors will be:
- Listed in the README
- Mentioned in release notes
- Credited in relevant documentation

Thank you for contributing to making professional networking more accessible and effective!

---

**Questions?** Open an issue or contact the maintainers.
