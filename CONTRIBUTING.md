# Contributing to BtechInAI

Thank you for your interest in contributing to BtechInAI! This is an open-source project dedicated to providing high-quality educational resources for AI students. Help from the community is essential to keeping our curriculum up-to-date and comprehensive.

## Table of Contents

- [How Can I Contribute?](#how-can-i-contribute)
- [Local Development Setup](#local-development-setup)
- [Contribution Workflow](#contribution-workflow)
- [How to Add or Update Curriculum Data](#how-to-add-or-update-curriculum-data)
- [Code Style Guidelines](#code-style-guidelines)
- [Community Guidelines](#community-guidelines)

---

## How Can I Contribute?

### Reporting Bugs
If you find a bug, please open an issue on GitHub. Include:
- A clear, descriptive title.
- Steps to reproduce the issue.
- Expected vs. actual behavior.
- Screenshots if applicable.

### Suggesting Enhancements
Have an idea for a new feature or a design improvement? Open an issue with:
- The goal of the enhancement.
- A detailed description of the proposed change.
- Any relevant context or examples.

### Adding Curriculum Data
Most of our contributions involve updating semester subjects, syllabi, or old question links. See the section below for details.

---

## Local Development Setup

BtechInAI is built using **Jekyll**. Follow these steps to run the site locally:

### 1. Prerequisites
Ensure you have the following installed:
- **Ruby** (2.7+ recommended)
- **Bundler** (`gem install bundler`)

### 2. Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/ashok936/btechinai.git
cd btechinai
bundle install
```

### 3. Run the Server
```bash
bundle exec jekyll serve
```
The site will be live at `http://localhost:4000`.

---

## Contribution Workflow

1. **Fork** the repository on GitHub.
2. **Clone** your fork locally.
3. **Create a branch** for your specific change:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Make your changes**. Ensure your code follows the minimalist design principles of the project.
5. **Commit** your changes with a clear message:
   ```bash
   git commit -m "Add syllabus for Semester III - Data Structures"
   ```
6. **Push** to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
7. **Open a Pull Request** against the `main` branch of the original repository.

---

## How to Add or Update Curriculum Data

The curriculum is managed in `index.md` and detailed syllabi are stored in the `/syllabus/` directory.

### To add/update subjects for a semester:
1. Open `index.md`.
2. Locate the corresponding semester ID (e.g., `sem3`).
3. Add a new `<div class="subject-item">` block using the following structure:
   ```html
   <div class="subject-item">
     <div class="subject-info">
       <h4><a href="/syllabus/course-code/">Subject Name</a></h4>
       <span class="subject-credits">X Credits</span>
     </div>
     <p class="subject-desc">Brief description of the course.</p>
     <div class="subject-links">
       <a href="/syllabus/course-code/">Syllabus</a>
       <a href="#">Old Questions</a>
     </div>
   </div>
   ```

### To add a new syllabus page:
1. Create a new markdown file in the `/syllabus/` directory (e.g., `syllabus/bt201co.md`).
2. Use the following frontmatter:
   ```yaml
   ---
   layout: default
   title: Subject Name
   course_code: BTXXX
   ---
   ```
3. Use the established HTML structure for units, examination schemes, and reference books.

---

## Code Style Guidelines

- **Minimalism**: Keep the design clean, black and white, and focus on readability.
- **Semantic HTML**: Use proper tags (`<section>`, `<article>`, `<h3>`) to ensure accessibility and SEO.
- **SCSS**: All styles should be added to `assets/main.scss` using CSS variables where appropriate.
- **Atomic Commits**: Keep your commits small and focused on a single change.

---

## Community Guidelines

By participating in this project, you agree to treat all contributors with respect. We aim to maintain a welcoming and inclusive environment for students and practitioners of all backgrounds.

---

*Thank you for helping us empower the next generation of AI scholars!*
