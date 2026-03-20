# Contributing Guide

Thanks for helping with the Kelvinspeech presentation! Here's the quickest path to contribution.

## Quick Start (5 minutes)

```bash
# 1. Clone the repo
git clone https://github.com/kwu-KKCC/Kelvinspeech.git
cd Kelvinspeech

# 2. Create a branch
git checkout -b feature/your-change

# 3. Make changes to index.html
# (Edit in your text editor)

# 4. Test - open index.html in your browser

# 5. Commit
git add index.html
git commit -m "feat: describe your change"

# 6. Push
git push origin feature/your-change
```

Then go to GitHub and create a Pull Request.

## Code Style

### Commit Messages

Use conventional commits:
- `feat:` - new feature or slide
- `fix:` - bug fix
- `style:` - styling/CSS changes
- `docs:` - documentation
- `ci:` - CI/CD changes

Example:
```
feat: add new feature

- Explain what you did
- Why you did it
- Any important details
```

### HTML Formatting

Keep consistent with existing code:
- Use 2-space indentation
- Match the style of nearby slides
- Use the color variable: `var(--gold)` not hex codes

### Testing

Before pushing:
1. Open `index.html` in your browser
2. Navigate all slides
3. Check your changes look good on different zoom levels
4. No broken layouts or missing text

## Slide Template

When adding a new slide, copy this structure:

```html
<!-- SLIDE N: TITLE -->
<section style="background: linear-gradient(135deg, rgba(15, 15, 30, 0.8) 0%, rgba(22, 33, 62, 0.8) 100%); font-size: 0.78em;">
  <h2 style="font-size: 2em; margin-bottom: 1.5em;">Your Title</h2>
  <div style="display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1.5em; max-width: 1300px; margin: 0 auto; padding: 0 1.5em;">

    <!-- Column 1 -->
    <div style="background: rgba(26, 26, 46, 0.9); padding: 1.5em; border-radius: 6px; border-top: 3px solid var(--gold);">
      <h3 style="color: var(--gold); font-size: 0.95em; margin-bottom: 1em; text-align: center;">Column Title</h3>
      <div style="font-size: 0.90em; line-height: 1.6;">
        <p style="margin-bottom: 0.8em;">Your content here</p>
      </div>
    </div>

    <!-- Column 2 -->
    <div style="background: rgba(26, 26, 46, 0.9); padding: 1.5em; border-radius: 6px; border-top: 3px solid var(--gold);">
      <h3 style="color: var(--gold); font-size: 0.95em; margin-bottom: 1em; text-align: center;">Column Title</h3>
      <div style="font-size: 0.90em; line-height: 1.6;">
        <p style="margin-bottom: 0.8em;">Your content here</p>
      </div>
    </div>

    <!-- Column 3 -->
    <div style="background: rgba(26, 26, 46, 0.9); padding: 1.5em; border-radius: 6px; border-top: 3px solid var(--gold);">
      <h3 style="color: var(--gold); font-size: 0.95em; margin-bottom: 1em; text-align: center;">Column Title</h3>
      <div style="font-size: 0.90em; line-height: 1.6;">
        <p style="margin-bottom: 0.8em;">Your content here</p>
      </div>
    </div>

  </div>
</section>
```

## Deployment

Don't worry about deployment! When your PR is merged to `main`:
1. GitHub Actions automatically triggers
2. Vercel builds and deploys
3. Changes go live within 60 seconds
4. Check https://speechslides-0324.vercel.app

## Questions?

- Check [README.md](README.md) for detailed setup
- Ask in GitHub Issues
- Contact Kelvin directly

## PR Checklist

Before submitting a PR:
- [ ] Changes are on a feature branch
- [ ] Code tested locally
- [ ] Commit messages are clear
- [ ] No unrelated changes included
- [ ] Updated README if needed

Thanks for contributing! 🎉
