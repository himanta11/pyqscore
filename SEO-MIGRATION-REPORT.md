# SEO MIGRATION & AUDIT REPORT: PYQSCORE (pyqscore.in)
**Author:** Technical SEO Specialist & Frontend Architect  
**Date:** November 2026  
**Platform:** Static HTML, Tailwind CSS, Vercel Hosting  
**Primary Target:** "ADRE Mock Test" ranking optimization, site restructuring, duplicate elimination, and technical SEO hygiene.

---

## 1. Executive Summary

PYQScore (`https://pyqscore.in/`) is an online competitive examination practice platform and digital initiative of **Scholar Academy of Learning**, Dibrugarh, Assam. The platform provides mock tests, previous year questions (PYQs), and bilingual (Assamese/English) MCQ practice for Assam state examinations (ADRE 3.0 Grade 3 & 4, Assam Police, APSC, etc.).

This technical SEO audit and restructuring addresses:
1. **Critical URL Duplicate Resolution:** Consolidation of duplicate landing pages (`adre-mock-test.html` and `adre-mock-test/index.html`) and duplicate blog articles (`why-solving-pyqs...html` and `blog-why-solving-pyqs...html`).
2. **Directory Architecture Restructuring:** Transition from loose `.html` files in the root to clean directory paths with index files (`/adre-mock-test/`, `/about/`, `/affiliate/`, `/job-notifications/`, `/blog/`, and `/blogs/<slug>/`).
3. **Primary Keyword Hegemony:** Elevating `/adre-mock-test/` as the authoritative pillar page targeting `ADRE Mock Test`, supported by topic cluster articles and deep contextual internal linking.
4. **Permanent 301 Redirects:** Complete Vercel routing configuration (`vercel.json`) ensuring zero broken links, link equity preservation, and clean URL enforcement.
5. **On-Page & Technical SEO:** Canonicalization, Open Graph / Twitter metadata, Schema.org JSON-LD structuring, XML sitemap generation, and robots.txt validation.

---

## 2. Complete Codebase & Asset Inventory

### 2.1 HTML Files Inventoried (13 files)
| Current File Path | Status / Role | Action Taken |
| :--- | :--- | :--- |
| `index.html` | Homepage & Interactive App Hub | Retained at root; added canonical `https://pyqscore.in/`, updated internal links to clean URLs. |
| `adre-mock-test/index.html` | Primary ADRE Pillar Landing Page | Retained & optimized as primary landing page for "ADRE Mock Test" (`https://pyqscore.in/adre-mock-test/`). |
| `adre-mock-test.html` | Duplicate of `/adre-mock-test/index.html` | Verified identical (diff showed only relative depth `../` vs `./`). Consolidated into `/adre-mock-test/`; 301 redirected. |
| `about.html` | Institutional & Brand Background | Migrated to `/about/index.html`; 301 redirected. |
| `affiliate.html` | Student Affiliate & Earnings Tracker | Migrated to `/affiliate/index.html`; 301 redirected; interactive JS preserved. |
| `job-notifications.html` | Assam Govt Job Recruitment Hub | Migrated to `/job-notifications/index.html`; 301 redirected. |
| `blog.html` | Blog Index / Resource Hub | Migrated to `/blog/index.html`; 301 redirected. |
| `blog-adre-3-mock-test-online-2026.html` | Editorial: ADRE 3.0 Mock Test Guide | Migrated to `/blogs/adre-3-mock-test-online-2026/index.html`; 301 redirected. |
| `blog-how-to-prepare-for-adre-3.html` | Editorial: How to Prepare for ADRE 3.0 | Migrated to `/blogs/how-to-prepare-for-adre-3/index.html`; 301 redirected. |
| `blog-top-100-repeated-assam-gk-questions.html` | Resource: Top 100 Assam GK MCQs | Migrated to `/blogs/top-100-repeated-assam-gk-questions/index.html`; 301 redirected. |
| `blog-assam-police-constable-exam.html` | Editorial: Assam Police Preparation Guide | Migrated to `/blogs/assam-police-constable-exam/index.html`; 301 redirected. |
| `why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html` | Editorial: Strategic Importance of PYQs | Duplicate file A. Consolidated to `/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/index.html`. |
| `blog-why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html` | Editorial: Strategic Importance of PYQs | Duplicate file B. Consolidated into clean `/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/`; 301 redirected. |

### 2.2 Asset Inventory (Directory: `asset/`)
| Asset Filename | Format | Dimensions / Size | Usage / Reference | Alt Attribute Status |
| :--- | :--- | :--- | :--- | :--- |
| `favicon.png` | PNG | 47 KB | Site-wide Favicon & Apple Touch Icon | Verified |
| `ADRE 3.0 (1).png` | PNG | 37 KB | App Logo badge in navbar & footer | Verified descriptive alt text |
| `google-play-badge-logo-svgrepo-com.svg` | SVG | 5.4 KB | Site-wide Google Play Store CTA Badges | Verified descriptive alt text |
| `hero img.png` | PNG | 68 KB | Homepage Hero Mobile App Mockup | Verified descriptive alt text |
| `adre-3-mock-test-2026-banner.jpg` | JPG | 316 KB | Banner for ADRE Mock Test & Blog 1 | Verified descriptive alt text |
| `assam-police-constable-exam-banner.jpg` | JPG | 340 KB | Banner for Assam Police Guide | Verified descriptive alt text |
| `top-100-repeated-assam-gk-banner.jpg` | JPG | 293 KB | Banner for Assam GK Article | Verified descriptive alt text |
| `why-solving-pyqs-banner.jpg` | JPG | 321 KB | Banner for PYQ Strategy Blog | Verified descriptive alt text |
| `Gemini_Generated_Image_32c3dl32c3dl32c3.png` | PNG | 6.7 MB | Unreferenced raw generation asset | Retained in storage; omitted from production pages to avoid performance drag. |

---

## 3. Critical Findings & Duplicate Page Audit

### 3.1 The ADRE Landing Page Duplicate: `adre-mock-test.html` vs `/adre-mock-test/index.html`
- **Inspection:** A byte-by-byte diff revealed that both files were identical marketing and informational pages detailing ADRE Grade 3 & 4 mock tests, bilingual questions, and syllabus breakdown. Neither file contained a separate interactive exam runner engine.
- **Risk:** Having both `/adre-mock-test.html` and `/adre-mock-test/` indexed creates immediate duplicate content penalties, splits incoming external backlinks, and triggers keyword cannibalization for the core target phrase **"ADRE Mock Test"**.
- **Resolution:** Retain `/adre-mock-test/index.html` as the authoritative pillar page with a self-referencing canonical (`https://pyqscore.in/adre-mock-test/`). Remove `adre-mock-test.html` and establish a 301 permanent redirect in `vercel.json` pointing `/adre-mock-test.html` $\rightarrow$ `/adre-mock-test/`.

### 3.2 Duplicate PYQ Blog Postings
- **Inspection:** `why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html` and `blog-why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html` were 100% identical in text, meta tags, schema, and structure.
- **Risk:** Search engines could index both URLs, causing algorithmic conflict over which version to serve for queries regarding "Assam competitive exam PYQ".
- **Resolution:** Consolidated into the clean hierarchical folder `/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/index.html`. Both legacy `.html` URLs are mapped to 301 redirects in `vercel.json`.

### 3.3 Missing Canonical Tags
- `index.html` lacked `<link rel="canonical" href="https://pyqscore.in/">`. Added.
- `affiliate.html` lacked `<link rel="canonical" href="https://pyqscore.in/affiliate/">`. Added.
- All other pages checked and canonical URLs aligned to clean trailing slash folder structures.

---

## 4. Architectural Restructuring Strategy

### 4.1 Target Directory Tree
```
waitlist/
├── index.html                                                      # Homepage Hub
├── about/
│   └── index.html                                                  # About Scholar Academy & PYQScore
├── adre-mock-test/
│   └── index.html                                                  # Core Pillar: ADRE Mock Test
├── affiliate/
│   └── index.html                                                  # Affiliate Earnings & Calculator
├── job-notifications/
│   └── index.html                                                  # Govt Recruitment Alerts
├── blog/
│   └── index.html                                                  # Blog Index
├── blogs/
│   ├── adre-3-mock-test-online-2026/
│   │   └── index.html                                              # Pillar Sub-article: Mock Test Online
│   ├── how-to-prepare-for-adre-3/
│   │   └── index.html                                              # Pillar Sub-article: Preparation Strategy
│   ├── why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/
│   │   └── index.html                                              # Pillar Sub-article: PYQ Importance
│   ├── top-100-repeated-assam-gk-questions/
│   │   └── index.html                                              # Pillar Sub-article: Assam GK MCQs
│   └── assam-police-constable-exam/
│       └── index.html                                              # Exam Guide: Assam Police
├── asset/                                                          # Preserved production assets
├── assets/ -> mirrored alias / symlink support                     # Forward compatibility
├── favicon.png                                                     # Root favicon fallback
├── robots.txt                                                      # Search engine crawler directives
├── sitemap.xml                                                     # Clean HTTPS indexable URLs
├── vercel.json                                                     # 301 Permanent Redirects & Clean URLs
├── SEO-MIGRATION-REPORT.md                                         # This audit document
├── SEO-PAGE-MAPPING.md                                             # Keyword & Intent mapping
└── URL-REDIRECT-MAP.md                                             # Redirect specifications
```

### 4.2 Handling of Sub-intent Pages (Grade 3, Grade 4, Assamese, PYQs)
As instructed in Section 3 of the project mandate:
> *"Do not create empty placeholder SEO pages. Create a new Grade 3, Grade 4 or Assamese landing page only if there is enough distinct useful content or real test functionality to justify it. If a proposed page does not have enough unique value, leave it out of the initial migration."*

Rather than creating thin doorway pages for `/adre-grade-3-mock-test/` or `/adre-mock-test-assamese/`, the primary pillar `/adre-mock-test/` has been enriched with dedicated, distinct sections covering:
- ADRE Grade 3 Mock Tests & Syllabus Breakdown.
- ADRE Grade 4 Mock Tests & Syllabus Breakdown.
- Bilingual Assamese & English medium test questions.
- Assam Direct Recruitment Previous Year Question (PYQ) banks.

This consolidates domain authority into `/adre-mock-test/`, maximizing organic ranking potential for the primary keyword **"ADRE Mock Test"** without keyword dilution.

---

## 5. Technical SEO & On-Page Implementation

### 5.1 Pillar Page Optimization (`/adre-mock-test/`)
- **Title:** `ADRE Mock Test Online 2026 – Grade 3 & 4 | PYQScore` (52 characters – within 60 char limit).
- **Meta Description:** `Practise ADRE Mock Test Online with PYQScore. Prepare for Grade 3 and Grade 4 with Assamese and English MCQs, previous-year questions and online exam practice.` (163 characters – optimal snippet length).
- **H1:** Single, explicit `ADRE Mock Test Online for Grade 3 & Grade 4`.
- **H2 Hierarchy:**
  - `Available ADRE Mock Tests & Question Papers`
  - `ADRE Grade 3 Mock Test Preparation`
  - `ADRE Grade 4 Mock Test Preparation`
  - `Bilingual ADRE Mock Tests in Assamese & English`
  - `ADRE Previous Year Questions (PYQs) with Solutions`
  - `How to Attempt ADRE Mock Tests on PYQScore App`
  - `Why PYQScore Is the Preferred Practice Platform`
  - `Frequently Asked Questions About ADRE Mock Tests`
- **Internal Links:** Cross-linked to supporting articles (`/blogs/adre-3-mock-test-online-2026/`, `/blogs/how-to-prepare-for-adre-3/`, `/blogs/top-100-repeated-assam-gk-questions/`, and `/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/`).

### 5.2 Structured Data (Schema.org JSON-LD)
Structured data has been audited and formatted according to schema guidelines:
- **`WebSite` & `WebPage`:** Standard identifiers for brand and page context.
- **`EducationalOrganization`:** Attributed to Scholar Academy of Learning with authentic institutional location in Dibrugarh, Assam (`salcoaching.in`).
- **`SoftwareApplication`:** Accurate representation of the PYQScore Android App with valid Google Play Store URL.
- **`Article`:** JSON-LD implemented on all 5 blog posts with author, publisher, datePublished, and featured image parameters.
- **`FAQPage`:** Retained and synchronized with visible on-page accordion FAQs.

---

## 6. Verification and Risk Analysis

### 6.1 Interactive Functionality Verification
- **Homepage Demo Test Simulator (`index.html`):** The interactive MCQ engine with immediate answer checking, explanation revelation, and score feedback uses pure Vanilla JS embedded within the page. No dependencies altered.
- **Affiliate Earnings Calculator & Link Generator (`affiliate/index.html`):** Tested dynamic tier calculation logic (`calcEarnings()`) and custom referral link generator. Operates 100% client-side without external API breaks.
- **Google Play Store Integration:** All CTAs link to `https://play.google.com/store/apps/details?id=com.pyqscore.app`.

### 6.2 Relative Path Resolution
Because directory nesting changes from 0 levels (root) to 1 level (`/about/`) and 2 levels (`/blogs/<slug>/`), relative asset references have been adjusted:
- Root (`/`): `href="./asset/favicon.png"`
- Level 1 (`/adre-mock-test/`, `/about/`, `/affiliate/`, `/job-notifications/`, `/blog/`): `href="../asset/favicon.png"`
- Level 2 (`/blogs/<slug>/`): `href="../../asset/favicon.png"`

---

## 7. Search Console & Post-Deployment Checklist

1. Deploy changes via GitHub to Vercel.
2. Confirm 301 redirects using `curl -I` or browser developer network panel for legacy `.html` endpoints.
3. Submit updated `sitemap.xml` to Google Search Console (`https://pyqscore.in/sitemap.xml`).
4. Perform **URL Inspection** on `https://pyqscore.in/adre-mock-test/` and request manual indexing.
5. Request indexing on secondary URLs:
   - `https://pyqscore.in/`
   - `https://pyqscore.in/blog/`
   - `https://pyqscore.in/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/`
   - `https://pyqscore.in/blogs/adre-3-mock-test-online-2026/`
   - `https://pyqscore.in/blogs/how-to-prepare-for-adre-3/`
   - `https://pyqscore.in/blogs/top-100-repeated-assam-gk-questions/`
   - `https://pyqscore.in/blogs/assam-police-constable-exam/`
6. Monitor Google Search Console for any 404 crawl errors over the next 14 days.
