 # aws-ai-practitioner-ml-flashcards

[![AWS AI Practitioner](https://img.shields.io/badge/AWS%20AI%20Practitioner-ff9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/certification/)
[![AI](https://img.shields.io/badge/AI-Machine%20Learning-blueviolet?style=for-the-badge)](https://en.wikipedia.org/wiki/Artificial_intelligence)

A small static site of ML/AI flashcards intended to help learn core concepts for the AWS AI Practitioner and related machine learning topics. The site is a single-page static HTML site (`index.html`) and is published via GitHub Pages.

Quick summary
- Repository: `aws-ai-practitioner-ml-flashcards` (renamed on GitHub)
- What it contains: `index.html` (the flashcards site)
- CI/CD: GitHub Actions workflow at `.github/workflows/ci-and-deploy.yml` validates `index.html` and deploys to GitHub Pages on pushes to `main`.

Preview locally

Open the `index.html` file in your browser, or serve it with a simple HTTP server from the project root:

```bash
# Python 3 simple server
python3 -m http.server 8000

# then open http://localhost:8000/index.html
```

Validate HTML (optional)

Requires Node.js for the validator. You can run a best-effort HTML check locally with:

```bash
# one-off with npx (no install required)
npx --yes html-validator --file=index.html --verbose || true
```

If you prefer to make validation strict (fail on errors) install `html-validator` as a dev dependency and remove the trailing `|| true`.

Contributing

- Make changes on a branch and open a PR. The workflow will run the validation job for PRs.
- When ready, merge to `main` to trigger deployment to GitHub Pages.

Notes

- If your site files move into a subfolder (for example `docs/` or a build output folder), update the Pages workflow `path:` to point to that folder.
- If your default branch is not `main`, update the workflow triggers accordingly.

Enjoy — let me know if you want the README expanded with a content map of the flashcards or a local build/test script.
