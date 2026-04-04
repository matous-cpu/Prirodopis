# Hravý Portál - Interaktivní Vzdělávání

A modular, interactive educational platform for middle school students.

## Project Overview
- **Goal:** Provide an engaging way for students to learn multiple subjects (Biology, History, etc.).
- **Structure:**
  - `web/`: The main directory containing the website.
  - `web/index.html`: The central hub linking to different subjects.
  - `web/biologie/`: Interactive biology textbooks and quizzes (7th/9th grade level).
  - `web/history/`: Future section for history lessons.
- **Tech Stack:** HTML5, CSS3, and Vanilla JavaScript.

## File Structure
- `web/index.html`: Main portal landing page.
- `web/biologie/index.html`: Biology dashboard.
- `web/biologie/app.html`: Advanced biology application with full features.
- `serve.sh`: Helper script to run a local webserver pointing to the `web/` folder.

## Development
To start the local development server:
```bash
bash serve.sh
```
