# Lucas1114.github.io

Personal portfolio. Static, no framework, served by GitHub Pages at
<https://lucas1114.github.io>.

It collects the projects listed below, each with the evidence that it works
rather than a description of what it is.

## Projects

Ordered by relevance to the roles I am looking for, not by date.

| Project | What it is | Evidence |
| --- | --- | --- |
| [rag-contract](https://github.com/Lucas1114/rag-contract) &middot; [live](https://rag-contract.fly.dev/) | Question answering over a fixed RFC corpus, built as a contract rather than a pipeline | recall@5 = 1.00, MRR 0.829; retrieval at 0.026 ms against a 150 ms deadline; a quality regression fails CI |
| [ai-incident-platform](https://github.com/Lucas1114/ai-incident-platform) &middot; [live](https://ai-incident-platform-152544821369.australia-southeast1.run.app/) | Turns an incident description into a structured investigation brief | Schema-constrained output validated by Pydantic; rate limited with 429 and `Retry-After`; deployed on Cloud Run with CI |
| [llm-inference-cp](https://github.com/Lucas1114/llm-inference-cp) &middot; [recording](https://asciinema.org/a/1265378) | A distributed control plane for LLM inference serving, in Go | One command induces a crash and a false positive; no request is lost, and duplicate results are adjudicated first-wins |
| [caseflow](https://github.com/Lucas1114/caseflow) &middot; [live](https://caseflow-frontend-production.up.railway.app) | A complete case-management slice from React to PostgreSQL | 25 backend tests; Flyway owns the schema; backend and database on private networking |
| [Visual-Algorithms](https://github.com/Lucas1114/Visual-Algorithms) &middot; [live](https://visual-algorithms-sandy.vercel.app) | Step-by-step animations of KMP, Manacher and Floyd cycle detection | Built twice, five years apart, with both versions deployed side by side |

## How the page is built

One `index.html` and one `style.css`. No framework, no build step, and nothing
loaded from another host &mdash; every image, the favicon and the Open Graph
card are served from this repository, so the page does not depend on a CDN
staying up.

The page is dark only and does not follow the system theme: four of the five
project screenshots are dark interfaces, so one committed surface is the look
the images already have. Each screenshot sits on a matte, which lets the one
light screenshot be framed the same way as the rest.

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
