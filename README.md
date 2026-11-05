# Math for Society

An open textbook by Benjamin D. Jackson for Walla Walla University's MATH 105, *Math for the Liberal Arts*. Written in [PreTeXt](https://pretextbook.org).

**Read it at <https://mathforsociety.org>.**

## License

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/), except for components listed on the book's Attributions page.

## Building

Source is in `source/`; build settings are in `project.ptx` and `publication/publication.ptx`.

```bash
pretext build web     # HTML, in output/web
pretext build print   # PDF
pretext view          # preview locally
```

PreTeXt is pinned in `requirements.txt`. Use lxml 6.0.x; lxml 6.1 breaks the build.

## Publishing

Pushing to `main` publishes the book. GitHub Actions (`.github/workflows/pretext-cli.yml`) builds it and deploys to GitHub Pages at mathforsociety.org.

CI cannot compile LaTeX diagrams. When you add or change a `latex-image`, build it locally (`pretext generate latex-image`) and commit the updated SVGs in `.cache/latex-image/`.
