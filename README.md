# Gemini 3 Context Repository

This repository contains a collection of `GEMINI.md` context files designed to enhance your AI-assisted development workflows with the Gemini CLI. These files provide specialized instructions, best practices, and personas for different domains.

## 📂 Available Contexts

### 1. [Senior Engineering](./senior-engineering/GEMINI.md)
**Focus:** General software architecture, clean code, refactoring, and debugging.
**Best For:** Complex coding tasks, architectural decisions, and maintaining code quality.

### 2. [Python & Web Specialist](./python-specialist/GEMINI.md)
**Focus:** Python development (environment, style, testing) and Modern Web Development (React, Next.js, TypeScript).
**Best For:** Full-stack development, Python backend work, and modern frontend applications.

### 3. [DevOps & Systems](./devops-engineer/GEMINI.md)
**Focus:** Operational safety, shell scripting, Docker, and CI/CD.
**Best For:** Infrastructure tasks, deployment scripts, and system administration.

### 4. [Database Engineering](./database/GEMINI.md)
**Focus:** SQL standards, schema design, performance optimization, and data safety.
**Best For:** Database migrations, query optimization, and schema planning.

### 5. [Creative Studio](./creative/GEMINI.md)
**Focus:** Prompt engineering, image generation, and asset management.
**Best For:** Generating assets, refining prompts, and creative workflows.

## 🚀 Usage

To use one of these contexts in your project:

1.  **Choose the context** that best fits your current task or project role.
2.  **Copy the file** to the root of your project (or the `.gemini/` directory if you prefer to keep it hidden).
3.  **Rename it** to `GEMINI.md`.

**Example:**
```bash
# For a Python web project
cp python-specialist/GEMINI.md /path/to/your/project/GEMINI.md
```

The Gemini CLI will automatically detect this file and use it to guide its responses, ensuring they align with the specific standards and practices defined therein.
