# Portfolio Customization Guide

This guide explains how to update and customize your portfolio website.

## Quick Updates

### Personal Information

Search for these placeholders in `index.html` and replace:

| Placeholder | Location | What to Update |
|-------------|----------|----------------|
| `lamingsrb@gmail.com` | Contact section | Your email |
| `+381 64 121 32 92` | Contact section | Your phone |
| `https://linkedin.com/in/your-profile` | Contact links | Your LinkedIn URL |
| `https://github.com/your-username` | Contact links | Your GitHub URL |
| `cv.pdf` | Hero CTA button | Path to your CV file |

### Profile Photo

Find this section in the About area:

```html
<!-- PLACEHOLDER: Replace with your actual photo -->
<div class="profile-placeholder">LM</div>
```

Replace with:

```html
<img src="your-photo.jpg" alt="Lazar Milicevic" style="width: 250px; height: 250px; border-radius: 50%; object-fit: cover;">
```

### Statistics

Update the counter targets in the About section:

```html
<div class="stat-number" data-target="10">0</div>  <!-- Years experience -->
<div class="stat-number" data-target="50">0</div>  <!-- Enterprise clients -->
<div class="stat-number" data-target="60">0</div>  <!-- Cost savings (k EUR) -->
```

## Content Updates

### Adding a New Job

In the Experience section, copy this template:

```html
<div class="timeline-item fade-in">
    <div class="timeline-content">
        <h3>Job Title</h3>
        <p class="company">Company Name</p>
        <p class="period">Start - End</p>
        <ul>
            <li>Achievement with metrics</li>
            <li>Another achievement</li>
        </ul>
    </div>
</div>
```

### Adding a New Project

In the Projects section, copy this template:

```html
<div class="project-card fade-in">
    <div class="project-image">ICON</div>
    <div class="project-info">
        <h3>Project Name</h3>
        <p>Brief description of the project.</p>
        <div class="project-tech">
            <span>Tech 1</span>
            <span>Tech 2</span>
        </div>
        <div class="project-impact">
            Key result or impact statement.
        </div>
    </div>
</div>
```

### Adding a Case Study

```html
<div class="case-study fade-in">
    <div class="case-study-header" onclick="toggleCaseStudy(this)">
        <h3>Case Study Title</h3>
        <span class="toggle">+</span>
    </div>
    <div class="case-study-content">
        <div class="case-study-body">
            <h4>Challenge</h4>
            <p>Describe the problem.</p>
            <h4>Approach</h4>
            <p>Describe your methodology.</p>
            <h4>Solution</h4>
            <p>Describe what you built/did.</p>
            <h4>Result</h4>
            <p>Describe outcomes with metrics.</p>
        </div>
    </div>
</div>
```

## Styling Changes

### Color Scheme

Colors are defined in CSS variables at the top of the `<style>` section:

```css
:root {
    --bg-primary: #0f1419;        /* Main background */
    --bg-secondary: #1a2332;      /* Section backgrounds */
    --bg-card: #1e2a3a;           /* Card backgrounds */
    --text-primary: #f1f5f9;      /* Main text */
    --text-secondary: #94a3b8;    /* Muted text */
    --accent: #2dd4bf;            /* Teal accent */
    --accent-hover: #14b8a6;      /* Accent hover state */
}
```

To change the accent color, update `--accent` and `--accent-hover` in both `:root` (dark mode) and `.light-mode` sections.

### Fonts

Change the Google Fonts import in `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
```

Then update the font-family:

```css
body {
    font-family: 'Inter', sans-serif;
}
```

### Adding Skills

In the Skills section, add a new skill bar:

```html
<div class="skill-bar">
    <div class="skill-info">
        <span class="skill-name">New Skill</span>
        <span class="skill-percent">85%</span>
    </div>
    <div class="skill-progress">
        <div class="skill-fill" data-width="85"></div>
    </div>
</div>
```

Add tech badges:

```html
<span class="tech-badge">New Technology</span>
```

## SEO Updates

Update the meta tags in `<head>`:

```html
<title>Your Name - Your Title</title>
<meta name="description" content="Your professional summary...">
<meta name="keywords" content="keyword1, keyword2, ...">
```

## Adding Your CV

1. Save your CV as `cv.pdf` in the same folder as `index.html`
2. The download button is already configured to link to it

## Testing Changes

1. Open `index.html` in your browser
2. Check responsive design by resizing window
3. Test dark/light mode toggle
4. Verify all links work
5. Test on mobile device

## Common Issues

**Skill bars not animating?**
- Make sure `data-width` attribute matches the percentage

**Counters not counting?**
- Check `data-target` attribute has the correct number

**Theme not saving?**
- Clear localStorage: `localStorage.clear()` in browser console

**Mobile menu not working?**
- Check that `toggleMenu()` function exists in JavaScript section

## Need Help?

If you encounter issues, check the browser console (F12) for errors.
