# How to contribute

Welcome! Community contributions are essential for keeping CarpoolVote running. We want to keep it as easy as possible to contribute changes. There are a few guidelines that we need contributors to follow so that we can have a chance of keeping on top of things.

## Philosophy

We want to keep this codebase as simple as we can, in order to encourage contributions from junior developers, and to help onboard new people quickly. That means avoiding technologies that junior developers might find overwhelming. For a long time our site was just static HTML, but as the website grew it became difficult to maintain without templating, so we've moved to Jekyll for static site generation. For client-side scripting we want to avoid newer, shinier, more advanced tools like React/Angular in favour of more beginner-friendly libraries like jQuery.

It's also very important that the site is accessible to disabled users. All HTML should be semantic and standards-compliant, and should use [WAI-ARIA](https://www.w3.org/WAI/intro/aria) and follow a11y best-practices wherever possible. We also prefer native HTML elements (e.g. `<button>` and `<input type="date"/>`) instead of bespoke UI controls wherever possible.

Our website should work on as many devices as possible. This means that it should be responsive and mobile-friendly design, as well as fast, lightweight, and performant. Assets should be kept as small as possible, and animations should be slick and unobtrusive. We try to support all browsers with >1% market share in the US - including IE11.

## Getting started

- Join our [Slack team](https://carpool-vote.slack.com/)! It's the best way to keep up to date with the project. Please [email us](mailto:slack@carpoolvote.com) if you would like to join.
- If you're new to GitHub and open-source, please familiarise yourself 
with the [official guidelines](https://guides.github.com/activities/contributing-to-open-source/).
- Check our GitHub issues to see what needs doing.
	- Read the full issue description and any discussion before beginning your work.
	- If the issue is unassigned, let us know if you want to take it, and we'll assign it you you.
	- If it is already assigned, then find a different issue.

## Working on the site

- The website is a static site, generated on deploy with [Jekyll](https://jekyllrb.com/), which is supported natively on Github Pages, our host. If you're unfamiliar with Jekyll, please have a quick read over the [documentation](https://jekyllrb.com/docs/home/).
- To work on it locally, you'll need to have Ruby installed on your machine, and install Jekyll.
- Once Jekyll is installed, you can start a local server using `jekyll serve`. To connect to the test API (instead of the live one), run `jekyll serve --config _config.yml,_config-dev.yml` instead.
- Please try to follow the existing code style:
	- 4 space indents
	- Double quotes on HTML attributes, single quotes for JS strings
	- HTML must be accessible and semantic
	- Cache your jQuery selectors if you're going to reuse them

## Making changes

- Fork the repository on GitHub
- Create a feature branch from where you want to base your work.
- Make commits of logical units.
- Check for unnecessary whitespace with `git diff --check` before committing.
- Make sure your [commit messages](https://github.com/erlang/otp/wiki/writing-good-commit-messages) 
clearly describe your change, are clear and concise, and are written in 
the imperative (e.g. 'Update rider email input field').
- Push your changes to a topic branch in your fork of the repository.
- Submit a pull request to this repository.

## Reviewing and testing PRs

- Once you have submitted a new PR, it will need to be reviewed and ideally tested before it's merged into master.
- Please indicate in your PR description whether your PR is ready to merge, or whether you're still working on it.
- Even if you have write permission to this repository, please try to avoid merging your own PRs, especially for large features.
- Ideally, every PR should have a senior project member sign off on it before being merged.
- If you have an urgent PR, please announce it in the #frontend or #backend Slack channel and one of us will try to prioritise reviewing and deploying it.
