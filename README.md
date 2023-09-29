# Edu Transformer

This repository powers our organization's website.

## Repository Structure

- `/source`: Contains the Hugo source files for our website.
- `/docs`: The built static content of our website, served directly via GitHub Pages.

## Local Development

For those looking to contribute or test changes locally:

1. Navigate to the `source` directory.
2. Run Hugo with `hugo server` to preview changes.
3. To build the static site, use `hugo --minify -d ../docs`.

## Publishing Changes Workflow

1. **Local Development**: Make changes in your Hugo `source` directory and test them locally.
2. **Local Build**: Build the static site with `hugo --minify -d ../docs`, which generates the static content in the `/docs` directory.
3. **Commit & Push**: Commit your changes to the `develop` branch and push to GitHub.
4. **Merge**: Once satisfied, merge changes from `develop` to `main`.
5. **Automatic Deployment**: GitHub Pages default pipeline detects the changes in `/docs` on the `main` branch and deploys the static site.

This setup has the advantage of simplicity. There's no need for an additional CI/CD process since the built content is committed directly to the repository, and GitHub Pages handles the deployment. Just a few things to keep in mind:

1. **Avoid Clutter**: Since you're committing both source and generated content, ensure that contributors or collaborators are aware of the setup to avoid confusion.
2. **Consistency**: Always use the same build process (`hugo --minify -d ../docs`) to maintain consistency.
