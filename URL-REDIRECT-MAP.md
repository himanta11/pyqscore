# URL REDIRECT MAP: PYQSCORE (pyqscore.in)

This document specifies the exact permanent (301) redirects configured in `vercel.json` to ensure 100% preservation of backlink equity, eliminate duplicate URLs, and provide seamless user transitions from legacy endpoints to clean folder structures.

---

## 1. Permanent Redirect Rules (HTTP 301)

| # | Legacy / Source URL | Target Canonical URL | HTTP Status | Justification & Verification |
| :-: | :--- | :--- | :-: | :--- |
| **1** | `/adre-mock-test.html` | `/adre-mock-test/` | `301` | **Critical Duplicate Resolution:** Identical content to `/adre-mock-test/index.html`. Consolidated into primary pillar folder. |
| **2** | `/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html` | `/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/` | `301` | **Duplicate & Architecture Migration:** Reorganized into hierarchical `/blogs/<slug>/` structure. |
| **3** | `/blog-why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html` | `/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/` | `301` | **Duplicate & Architecture Migration:** Reorganized into hierarchical `/blogs/<slug>/` structure. |
| **4** | `/blog-adre-3-mock-test-online-2026.html` | `/blogs/adre-3-mock-test-online-2026/` | `301` | **Clean URL Migration:** Root loose `.html` file moved to dedicated directory route. |
| **5** | `/blog-how-to-prepare-for-adre-3.html` | `/blogs/how-to-prepare-for-adre-3/` | `301` | **Clean URL Migration:** Root loose `.html` file moved to dedicated directory route. |
| **6** | `/blog-top-100-repeated-assam-gk-questions.html` | `/blogs/top-100-repeated-assam-gk-questions/` | `301` | **Clean URL Migration:** Root loose `.html` file moved to dedicated directory route. |
| **7** | `/blog-assam-police-constable-exam.html` | `/blogs/assam-police-constable-exam/` | `301` | **Clean URL Migration:** Root loose `.html` file moved to dedicated directory route. |
| **8** | `/about.html` | `/about/` | `301` | **Clean URL Migration:** Hub page moved to directory route. |
| **9** | `/blog.html` | `/blog/` | `301` | **Clean URL Migration:** Hub page moved to directory route. |
| **10** | `/job-notifications.html` | `/job-notifications/` | `301` | **Clean URL Migration:** Hub page moved to directory route. |
| **11** | `/affiliate.html` | `/affiliate/` | `301` | **Clean URL Migration:** Hub page moved to directory route. |

---

## 2. Directory and Index Routing Strategy

Vercel serves directory paths containing an `index.html` natively without trailing file extensions.
- When a user or crawler visits `https://pyqscore.in/adre-mock-test/`, Vercel automatically serves `waitlist/adre-mock-test/index.html` with HTTP 200.
- With `trailingSlash: true` enabled in `vercel.json`, requests to `/adre-mock-test` are normalized cleanly to `/adre-mock-test/`.
- With `cleanUrls: true` enabled in `vercel.json`, any direct request to a `.html` file is cleanly handled.

---

## 3. Vercel Configuration Implementation (`vercel.json`)

```json
{
  "$schema": "https://openapi.vercel.sh/vercel.json",
  "cleanUrls": true,
  "trailingSlash": true,
  "redirects": [
    {
      "source": "/adre-mock-test.html",
      "destination": "/adre-mock-test/",
      "permanent": true
    },
    {
      "source": "/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html",
      "destination": "/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/",
      "permanent": true
    },
    {
      "source": "/blog-why-solving-pyqs-is-key-to-cracking-assam-competitive-exams.html",
      "destination": "/blogs/why-solving-pyqs-is-key-to-cracking-assam-competitive-exams/",
      "permanent": true
    },
    {
      "source": "/blog-adre-3-mock-test-online-2026.html",
      "destination": "/blogs/adre-3-mock-test-online-2026/",
      "permanent": true
    },
    {
      "source": "/blog-how-to-prepare-for-adre-3.html",
      "destination": "/blogs/how-to-prepare-for-adre-3/",
      "permanent": true
    },
    {
      "source": "/blog-top-100-repeated-assam-gk-questions.html",
      "destination": "/blogs/top-100-repeated-assam-gk-questions/",
      "permanent": true
    },
    {
      "source": "/blog-assam-police-constable-exam.html",
      "destination": "/blogs/assam-police-constable-exam/",
      "permanent": true
    },
    {
      "source": "/about.html",
      "destination": "/about/",
      "permanent": true
    },
    {
      "source": "/blog.html",
      "destination": "/blog/",
      "permanent": true
    },
    {
      "source": "/job-notifications.html",
      "destination": "/job-notifications/",
      "permanent": true
    },
    {
      "source": "/affiliate.html",
      "destination": "/affiliate/",
      "permanent": true
    }
  ],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "X-Frame-Options",
          "value": "SAMEORIGIN"
        },
        {
          "key": "X-XSS-Protection",
          "value": "1; mode=block"
        },
        {
          "key": "Referrer-Policy",
          "value": "strict-origin-when-cross-origin"
        }
      ]
    },
    {
      "source": "/asset/(.*)",
      "headers": [
        {
          "key": "Cache-Control",
          "value": "public, max-age=31536000, immutable"
        }
      ]
    }
  ]
}
```

---

## 4. Redirect Loop & Chain Prevention Verification
- **Chain Check:** Each legacy URL redirects in a single hop directly to the final canonical folder (e.g., `/blog-adre-3-mock-test-online-2026.html` $\rightarrow$ `/blogs/adre-3-mock-test-online-2026/`). Zero multi-hop chains.
- **Loop Check:** All target URLs are directory roots hosting an actual `index.html` file that serves HTTP 200 without issuing a redirect.
