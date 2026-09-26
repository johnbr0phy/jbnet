# Lighthouse baseline (before head video)

Lighthouse 12, performance only, local static server, 2026-09-26.

| Run | Score | LCP | CLS | FCP | TBT |
|---|---|---|---|---|---|
| Mobile | 59 | 25.4 s | 0.116 | 1.4 s | 460 ms |
| Desktop | 81 | 3.5 s | 0 | 0.3 s | 10 ms |

- Mobile LCP element: `images/ai-creations/the-bicycle.jpg`. Desktop LCP element: a `<p>`.
- Page weight 12.6 MB. Largest: `images/adventures/02-montreal.gif` (3.3 MB).
- 5.3 MB of the load is the 32 head-tracker stills (832x1248 JPEGs shown at 156px), all preloaded by script. The largest is `white-center.jpg` at 433 KB.
