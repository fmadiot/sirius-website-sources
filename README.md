# Eclipse Srius Website Sources

Sources of the [Eclipse Sirius](https://projects.eclipse.org/projects/modeling.sirius) website at https://eclipse.dev/sirius.

This repository contains the [Jekyll](https://jekyllrb.com) templates used to generate the actual content of the Eclipse Sirius website.

The result of the Jekyll build (inside the `sirius` folder) should be pushed to the `master` branch of https://github.com/eclipse-sirius/sirius-website where they will be picked up by the Eclipse Foundation's tools and deployed at https://eclipse.dev/sirius.

## Building

To build the website locally:

1. Make sure you have Ruby and Bundler installed (tested with Ruby 3.2.2 and Bundler 2.4.10).
2. Use Bundler to install the required dependencies (needed only the first time or when dependencies are changed):

        bundle install

3. Build the website:

        bundle exec jekyll build

The result is available inside the `_site/sirius` directory.

To facilitate tracking the changes, the result of the build is commited into git.

## Deploying manually

1. Get a clone of https://github.com/eclipse-sirius/sirius-website, which corresponds to the content that will actually be deployed and made visible at https://eclipse.dev/sirius.
2. *Replace* the contents of the `main` branch from that clone with the result of the build obtained in `_site/sirius` (see above). Note that the Jekyll templates here produce the result inside a `sirius` directory. Only the *contents* inside that directory should be commited into `eclipse-sirius/sirius-website`.
3. Commit and push.

Wait a few minutes, and the new content will soon be available at https://eclipse.dev/sirius.
