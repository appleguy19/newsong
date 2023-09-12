[![Netlify Status](https://api.netlify.com/api/v1/badges/6e252336-5098-4be5-8293-997c2dfd75fa/deploy-status)](https://app.netlify.com/sites/newsong/deploys)

# About

This is the repo for Newsong's new website.

### For Developers

To work on the Newsong website you should be familiar with the following technologies:

- Yarn
- Git
- SCSS
- HTML
- JavaScript

#### Grab the Code

0. Install and [configure Git](https://help.github.com/articles/set-up-git/)

1. [Set up an SSH key](https://help.github.com/articles/generating-ssh-keys/)

2. Clone the repository: `git clone git@github.com:appleguy19/newsong.git`

#### Set up Software

0. Install [Homebrew](http://brew.sh/)

1. Install Node via Homebrew: `brew install node`

2. Install Yarn via Homebrew: `brew install yarn`

3. `cd` to this directory and install dependencies: `yarn install`

### Running the Scripts

Everything you need to build this site can be done with Yarn Scripts and bundler. Check the `package.json` file for a list of all the yarn scripts you can run. Check the `Gemfile` for the details on ruby gems. Here are some that you're sure to use.

0. Compile and begin watching Sass/SCSS: `yarn run css-watch`

1. To build for local testing: `yarn run css-build && bundle exec jekyll serve`

### Deploying this website

0. Create a branch.

1. Commit changes to that branch.

2. Create a Pull Request (into `master`). Remember to reference a Github Issue if there is one. The PR will get a staging branch on Netlify automatically. You can use this for testing.

3. Once the PR is merged into `master` the site will be automatically deployed via [Netlify](https://netlify.com) to https://newsong-fellowship.com

#### Git Hooks

It is very helpful to have a [pre-commit hook to optimize images](https://nchristiny.com/blog/command-line-image-optimization) using [imageoptim-cli](https://github.com/JamieMason/ImageOptim-CLI). Add this snippet below to accomplish this.

```
images=$(git diff --exit-code --cached --name-only --diff-filter=ACM -- '*.png' '*.jpg')
$(exit $?) || (echo "$images" | imageoptim -a && git add $images)
```
