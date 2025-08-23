# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **resume creation toolkit** based on the LapisCV project by Bingyan Studio. It's an Obsidian vault configured to create professional resumes using Markdown with custom CSS styling and embedded fonts.

**This is NOT a traditional software project** - it has no build scripts, package.json, or test suite. Instead, it's a document creation system optimized for resume/CV generation.

## Key Components

### Resume Files
- `template-cn.md` / `template-en.md`: Base templates for Chinese/English resumes
- `resume-cn.md`: Current working resume file
- `oldCV.md`: Previous resume version for reference

### Styling System
- `.obsidian/snippets/lapis-cv.css`: Main theme with embedded Chinese fonts (SourceHanSansCN, JetBrainsMono)
- `.obsidian/snippets/lapis-cv-serif.css`: Serif variant theme
- Both CSS files are ~45MB due to embedded fonts for self-contained operation

### Configuration
- `.obsidian/app.json`: PDF export settings (A4, 1mm margins, 98% downscale)
- `.obsidian/appearance.json`: Theme configuration (Moonstone theme, accent color #4870ac)

## Common Operations

### Editing Resumes
- Edit markdown files directly (`template-cn.md`, `resume-cn.md`, etc.)
- Use standard markdown syntax with HTML elements for styling
- Icons use custom font: `<span class="icon">&#xe60f;</span>` for phone, `<span class="icon">&#xe7ca;</span>` for email
- Section headers: `## <span>&#xe80c;</span> 教育经历`

### Styling Customization
- Modify CSS variables in `.obsidian/snippets/lapis-cv.css`:
  - `--accent-color`: Main theme color (#4870ad)
  - `--avatar-width`: Profile image size
  - `--text-color`: Main text color (#353a42)
- To make avatar square instead of circular: change `border-radius: 50%` to `border-radius: 0`
- Always comment out old CSS rules instead of deleting them

### Content Structure
- Use `<div class="entry-title">` for project/job headers with dates
- Profile image: `<img class="avatar" src="filename.jpg">`
- Contact info uses icon spans with specific Unicode characters
- Technical skills organized in nested lists with **bold** keywords

### PDF Export
- Use Obsidian's built-in PDF export (Ctrl+P)
- Settings are pre-configured in `.obsidian/app.json`
- Export is optimized for A4 printing with professional margins

## Architecture Notes

### Font System
- Self-contained with embedded Chinese fonts (SourceHanSansCN, SourceHanSerifCN)
- Custom icon font (LapisCV Icon) for UI elements
- JetBrainsMono for code/technical text
- No external font dependencies

### Color Scheme
- Primary accent: #4870ad (professional blue)
- Text: #353a42 (dark gray for readability)
- Borders: #dae3ea (subtle gray)
- All colors defined as CSS variables for easy customization

### Layout System
- Uses CSS Grid and Flexbox for responsive design
- Optimized for PDF export, not web display
- Right-aligned avatar with floating positioning
- Entry titles use flex layout for title/date alignment

## File Naming Conventions
- Templates: `template-{lang}.md`
- Working files: `resume-{lang}.md` or descriptive names
- Images: Place in root directory, reference directly by filename
- Backup files: Keep with descriptive names like `oldCV.md`

## Current User Context
The user is a Java backend developer intern with experience in:
- Spring ecosystem (SpringBoot, MyBatis, Spring AOP)
- Database technologies (MySQL, Redis)
- Distributed systems and microservices
- Open source contributions (cap4j framework)

When making changes, maintain professional formatting and technical accuracy for software engineering roles.