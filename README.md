# About

This is the repo for Newsong's new website.


### For Developers

To work on the Newsong website you should be familar with the following technologies:

 - Yarn
 - Git
 - SCSS
 - HTML
 - JavaScript

#### Grab the Code

0. Install and [configure Git](https://help.github.com/articles/set-up-git/)

0. [Set up an SSH key](https://help.github.com/articles/generating-ssh-keys/)

0. Clone the repository: `git clone git@github.com:appleguy19/newsong.git`

#### Set up Software

0. Install [Homebrew](http://brew.sh/)

0. Install Node.js via Homebrew: `brew install node`

0. Install Ruby via Homebrew: `brew install yarn`

0. Install dependencies: `yarn`

### Running the Scripts

Everything you need to build this site can be done with Yarn Scripts. Check the `package.json` file for a list of all the scripts you can run. Here are some that you're sure to use.

0. Compile and begin watching Sass/SCSS: `yarn run css-watch`

0. To build for production: `yarn run css-build`

#### Git Hooks

There is a [pre-commit hook to optimize images](https://github.com/JamieMason/ImageOptim-CLI#adding-to-git-pre-commit-hook) using imageOptim-cli

```
images=$(git diff --exit-code --cached --name-only --diff-filter=ACM -- '*.png' '*.jpg')
$(exit $?) || (echo "$images" | imageOptim -a -q && git add $images)
```
