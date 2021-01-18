# switches

With mobile browsers as our canvas, performance is always an issue. It's crucial for the page to only load what it needs, and nothing more.

Jekyll uses frontmatter for page requirements. We created a `page.switches` variable, where each tag activates an `if` function on [`default.html`](https://github.com/nonlinear/nonlinear.github.io/blob/master/_layouts/default.html) layout, when listed.

Visit [nonlinear.nyc/switches](https://www.nonlinear.nyc/switches/) for the updated list.

## Install as a submodule

Go to the folder on your project you want to add switches folder (for instance, `_includes/` if you use jekyll), then run `git submodule add https://github.com/nonlinear/switches.git switches`

## Troubleshoot: jekyll submodule + githubpages

Github generates jekyll server-side, and submodule breaks because it renames folder with commit. Jekyll is meant to be client-side, so there's a way to prevent github from rebuilding it server-side:

1. force jekyll to generate flat blog on `docs/` folder, instead of default `_site/` by adding `destination: docs` on `config.yml`
1. push changes
1. on github settings, tell githubpages to point to `docs/` folder instead