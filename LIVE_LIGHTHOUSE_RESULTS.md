# Live Lighthouse Results

Lighthouse 12.8.2 was run against the deployed GitHub Pages URLs. Scores are category scores from the saved JSON reports.

| Page | Performance | Accessibility | Best Practices | SEO | All >90 |
| --- | ---: | ---: | ---: | ---: | --- |
| `index.html` | 96 | 95 | 96 | 100 | PASS |
| `chambres.html` | 98 | 96 | 96 | 100 | PASS |
| `experiences.html` | 96 | 96 | 96 | 100 | PASS |
| `galerie.html` | 97 | 95 | 96 | 100 | PASS |
| `contact.html` | 97 | 96 | 96 | 100 | PASS |

The homepage report reflects the post-deployment performance fix in commit `807e5ad`; the other four pages were unchanged by that fix and use their live reports from the same audit batch.

## Raw reports

- `/home/ubuntu/lighthouse-live-index-postfix.json` — ok
- `/home/ubuntu/lighthouse-live-chambres.json` — ok
- `/home/ubuntu/lighthouse-live-experiences.json` — ok
- `/home/ubuntu/lighthouse-live-galerie.json` — ok
- `/home/ubuntu/lighthouse-live-contact.json` — ok
