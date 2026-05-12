# China Mobile Technical Research Template - Design Specification

> Suitable for China Mobile technical research reports, model evaluations, technology trend studies, solution research, and internal capability briefings.

---

## I. Template Overview

| Property | Description |
| --- | --- |
| **Template Name** | china_mobile_research |
| **Use Cases** | China Mobile technical research, technology evaluation, architecture analysis, internal decision briefings |
| **Design Tone** | Conclusion-first, information-dense, structured, restrained, enterprise-telecom |
| **Theme Mode** | Light theme (white background + China Mobile blue accents) |

---

## II. Canvas Specification

| Property | Value |
| --- | --- |
| **Format** | Standard 16:9 |
| **Dimensions** | 1280 x 720 px |
| **viewBox** | `0 0 1280 720` |
| **Page Margins** | Left/Right 60px, Top 80px, Bottom 40px |
| **Safe Area** | x: 60-1220, y: 80-680 |

---

## III. Color Scheme

### Primary Colors

| Role | Value | Notes |
| --- | --- | --- |
| **China Mobile Blue** | `#0050B3` | Titles, section blocks, core emphasis |
| **Bright Support Blue** | `#00B4D8` | Decorative highlights, guide lines, accent elements |
| **Deep Ocean Blue** | `#003366` | Chapter / cover dark backgrounds |
| **Light Telecom Blue** | `#E6F4FF` | Secondary panels, soft section backgrounds |

### Text Colors

| Role | Value | Usage |
| --- | --- | --- |
| **Primary Text** | `#1A1A1A` | Titles, body text |
| **Secondary Text** | `#4A5568` | Notes, support copy |
| **Auxiliary Text** | `#718096` | Page numbers, footer, annotations |
| **White Text** | `#FFFFFF` | Text on dark backgrounds |

### Functional Colors

| Usage | Value | Description |
| --- | --- | --- |
| **Judgment Red** | `#D93A49` | Key risks, decisive judgments, negative changes |
| **Positive Green** | `#38A169` | Positive trend, completion, support signals |
| **Neutral Divider** | `#D9E2EC` | Border lines, dashed separators |

---

## IV. Typography System

### Font Stack

**Font Stack**: `"Microsoft YaHei", "微软雅黑", SimHei, Arial, sans-serif`

### Font Size Hierarchy

| Level | Usage | Size | Weight |
| --- | --- | --- | --- |
| H1 | Cover main title | 52px | Bold |
| H2 | Page title | 28px | Bold |
| H3 | Section title / module title | 22-24px | Bold |
| P | Body content | 16-18px | Regular |
| Data | Highlighted number | 34-40px | Bold |
| Sub | Annotation / footer | 12-14px | Regular |

---

## V. Page Structure

### General Layout

| Area | Position/Height | Description |
| --- | --- | --- |
| **Top** | y=0, h=6px | Blue gradient bar |
| **Title Bar** | y=30, h=50px | Section number block + page title + org area |
| **Content Area** | y=100, h=560px | Main content area |
| **Footer** | y=680, h=40px | Page number, org short name, bottom line |

### Research Page Expectations

- Default to high information density
- Each content page should carry one visible page-level judgment
- Prefer evidence modules, comparison blocks, diagram + explanation, and case grids over sparse generic cards
- Chapter pages should read as directory pages, not only title dividers

---

## VI. Page Types

### 1. Cover Page (`01_cover.svg`)

- Dark blue technology cover
- Large conclusion-oriented title
- Presenter / organization / date block
- Suitable for internal research briefings

### 2. Table of Contents (`02_toc.svg`)

- Directory-style overview page
- Supports 4-6 chapters
- Highlights the report's structure and judgment flow

### 3. Chapter Page (`02_chapter.svg`)

- Strong chapter transition
- Large chapter number + title
- Suitable before each major section

### 4. Content Pages

- `03_content.svg`: generic dense research shell with title bar, summary strip, left observation sidebar, and main content zone
- `03a_content_evidence.svg`: evidence mosaic
- `03b_content_compare.svg`: comparison table + verdict sidebars
- `03c_content_architecture.svg`: architecture row + explanation blocks
- `03d_content_case_grid.svg`: observation bar + case grid + final judgment

### 5. Ending Page (`04_ending.svg`)

- Thank-you / summary ending
- Suitable for internal next-step and discussion closing

---

## VII. Recommended Patterns

- Research evidence mosaic
- Comparison table + verdict sidebar
- Architecture evolution + explanation blocks
- Observation bar + case grid + judgment strip
- Metrics cluster + support modules
- Summary cards + recommendation grid

These patterns should map to the content-page variants above whenever possible, instead of forcing every page through a single generic content shell.

---

## VIII. SVG Technical Constraints

1. viewBox: `0 0 1280 720`
2. Use `<rect>` for page backgrounds
3. Use `<tspan>` for wrapped or emphasized text
4. Use HEX colors and `fill-opacity` / `stroke-opacity`; `rgba()` is forbidden
5. Prohibited: `mask`, `<style>`, `class`, `foreignObject`, `textPath`, `animate*`, `script`
6. `clipPath` is allowed only on `<image>` under shared standards
7. `marker-start` / `marker-end` follow shared standards only

---

## IX. Placeholder Specification

| Placeholder | Description |
| --- | --- |
| `{{TITLE}}` | Main title |
| `{{SUBTITLE}}` | Subtitle |
| `{{PRESENTER}}` | Presenter |
| `{{ORGANIZATION}}` | Full organization name |
| `{{ORG_SHORT}}` | Short organization name |
| `{{DATE}}` | Date |
| `{{PAGE_TITLE}}` | Page title |
| `{{CHAPTER_NUM}}` | Chapter number |
| `{{PAGE_NUM}}` | Page number |
| `{{CONTENT_AREA}}` | Flexible content zone |
