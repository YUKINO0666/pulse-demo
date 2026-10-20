# PULSE — Post-Quantum IoT Crypto Demos

3 single-file HTML artifacts demoing PULSE, a post-quantum crypto SDK for IoT edge devices.

| Demo | Purpose |
|---|---|
| [landing-demo.html](landing-demo.html) | Marketing overview — why migrate now, 6 SDK features, key-exchange flow, real benchmark numbers, customer testimonial |
| [onboarding-wizard.html](onboarding-wizard.html) | 4-step device enrollment wizard (device profile → credentials → algo/rotation → deploy) |
| [spectrum-analyzer.html](spectrum-analyzer.html) | Live RF spectrum dashboard — band filters, animated spectrum chart, anomaly detections, real-time alert feed |

All 3 are wired together: pick a device in the wizard → land on the spectrum analyzer with the device context pre-loaded (`localStorage` handoff + `?from=` query param for analytics).

## Stack

- **Zero build** — single-file HTML, no bundler, no `npm install`
- **Vanilla CSS + JS** — design tokens via CSS variables, no framework
- **Driver.js 1.0.1** — product tour via CDN (only spectrum-analyzer)
- **Inter** — Google Fonts

## Local preview

```bash
python3 -m http.server 8766 --directory .
# open http://localhost:8766/landing-demo.html
```

## Deploy

Any static host works — GitHub Pages, Cloudflare Pages, Netlify, S3+CloudFront, plain nginx.
No server-side logic; everything runs in the browser.

## License

Demo / evaluation use.