---
name: edu-page-generator
description: Fetches educational data from Wikipedia, summarizes it in Czech, and generates themed sub-pages for the "Hravý přírodopis 7" project.
---

# Educational Page Generator

This skill automates the creation of detailed sub-pages for the "Hravý přírodopis 7" project by fetching data from Wikipedia and formatting it into a consistent HTML structure.

## Workflow

1.  **Fetch Data**: Use `web_fetch` on the provided Wikipedia URL. Request a detailed summary including characteristics, anatomy, and diversity.
2.  **Summarize in Czech**: Translate and summarize the information in Czech (čeština). Ensure it's suitable for a 7th-grade student level.
3.  **Generate Page**:
    *   Read `assets/edu-page-template.html` from this skill's directory.
    *   Replace placeholders:
        *   `{{TITLE}}`: The subject name (e.g., "Ptáci").
        *   `{{ICON}}`: A relevant emoji (e.g., "🦅").
        *   `{{SUBTITLE}}`: A catchy one-sentence description.
        *   `{{CONTENT}}`: The summarized Czech text formatted with `<h2>`, `<h3>`, `<ul>`, and `<p>` tags.
    *   Save as `[subject_name].html` (e.g., `ptaci.html`).
4.  **Update Navigation**:
    *   In `index.html` and `app.html`, find the corresponding section.
    *   Make the container clickable using `onclick="location.href='[subject_name].html'"` (if applicable).
    *   Add a "Více info" button that links to the new page.
    *   Use `event.stopPropagation()` on buttons within the container to prevent double-triggering clicks.
5.  **Commit Changes**:
    *   Once the new sub-page is created and navigation is updated, stage all changes.
    *   Commit the changes with a descriptive message like "Add detailed page for [Subject Name]".
    *   Verify the commit with `git status`.

## Templates

The base template is located at `assets/edu-page-template.html`. It contains the project's default styling (green gradients, white containers, and responsive layout).

## Best Practices

*   Keep the language simple but scientifically accurate.
*   Always include a "Zajímavost" (fun fact) in a `<div class="highlight">` block.
*   Ensure the "Zpět na hlavní stránku" links correctly point to `index.html`.
