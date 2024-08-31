# /dev/mtl 2024

The /dev/mtl 2024 website is a static site compiled with [Jekyll](https://jekyllrb.com/docs/home/). The frontend relies heavily on the [Foundation](http://foundation.zurb.com/sites/docs/) framework. Frontend dependencies are installed and updated with [npm](https://www.npmjs.com/).

## Code of Conduct

As a contributor, you can help us keep the community open and inclusive.
Please read and follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## Getting Started

Get started contributing by reading our [Contributing](CONTRIBUTING.md) guidelines.

### Contributing via Browser

1. Navigate to the [/dev/mtl](https://github.com/devmtl2024/site) on GitHub. In the upper right hand corner of the repo, click the "Fork" button. Alternatively, click on an individual file and click the pencil icon. GitHub will automatically fork the repo for you.

2. Head over to your GitHub account, where you will find the forked repo. This is a copy of the official code. Your changes to this forked code will not affect the official code, unless you submit a pull request and an admin merges your pull request.

3. For changes that do not need to be tested locally, the change can be made and submitted in the browser.

4. Within your forked repo, make sure the "Branch" tab is set to the `main` branch.

5. Once you are on the correct branch, navigate to the file you intend to change and click the pencil icon to open it. Make the change and click the "Commit changes" button.

6. Staying within your forked repo, navigate back to the main page of the branch (note: your pull request should be submitted via your forked repo, not the main repo). Click "New pull request." Click the "Commit changes" button. At the "Comparing changes" page, double check that you are happy with your proposed change. If so, click "Create pull request." Add a descriptive title and comment if applicable, then click "Create pull request" at the bottom to submit. An admin will review your proposed change, merge it, or give you feedback. If you are not ready for your pull request to be immediately merged, you can let those reviewing pull requests know by using the acronym WIP (Work in Progress) or a similar message in your pull request title.

#### Example: Updating Organizer Info

Follow the above instructions to step 5.

Click on the `_organizer` folder, then your own `MY_NAME.md` file. Click on the pencil icon to open the file. Make your changes, making sure that your information is placed within quotation marks.

**To add a photo:** navigate to the `static/img/organizers` folder. Click "Upload files". Drag or choose your photo file into the window. Click "Commit changes". Your photo should now be in the folder. Ideally, the photo should be 400 x 400px. In your `MY_NAME.md` file, make sure the path to your photo has the proper name and file ending (`.jpg`, `.png`, etc.).

If you need assistance, please ask! Complete step 6.

### Contributing via Local Development

For changes that require cloning/running the code locally, follow the above instructions to step 5. Instead of navigating to the file through the browser, open up your computer terminal (you will need to have Git installed locally and a code editor of your choice).

Clone your forked repo locally via the terminal, replacing the username in the URL with your own (note: not all operating systems will use a `$` as a terminal prompt).

```bash
$ git clone https://github.com/<your-username>/devmtl2024
```

Change directory into the folder

```bash
$ cd devmtl2024
```

Verify that you are on the `main` branch

```bash
$ git branch
```

Follow the instructions below to run the website on a local server. GitHub recommends using [Bundler](http://bundler.io/) to install and run Jekyll. [Ruby](https://www.ruby-lang.org) is a pre-requisite. One of the project dependencies (nokogiri) requires a Ruby version >= 2.1.0. See the [Jekyll Quick-start Guide](https://jekyllrb.com/docs/quickstart/) for more info.

#### Install Jekyll

You might need to use ```sudo gem install jekyll bundler foreman```.

```bash
gem install jekyll bundler
bundle install
```

##### Use local installation on Debian-like

Use [rbenv](https://github.com/rbenv/rbenv).

```bash
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
~/.rbenv/bin/rbenv init
```

Bash or source or reload a terminal, and cd to the directory of this project.

```bash
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
rbenv install 3.1.6
rbenv local 3.1.6
gem install bundler jekyll
bundle install
```

#### Install Node Dependencies

You will need Node v10.0 or greater to compile frontend assets. We're using [Webpack](https://webpack.js.org/) to compile Scss and JavaScript.

You'll need to install all the JS dependencies.

```bash
$ npm install .
# installs dependencies listed in package.json
```

#### Compile CSS & JS

```bash
$ npm run build
# Builds production-ready assets
```

#### Run Jekyll

```bash
$ bundle exec jekyll serve
# => Now browse to http://localhost:4000
```

#### Run html-proofer to find broken links and accessibility issues

```bash
$ bundle exec rake test
```

#### Pushing to GitHub and Submitting a Pull Request

After you have made your changes, you will need to push the local files with the changes back to GitHub in order to submit a pull request. Assuming you are still on the `main` branch, you will be pushing your changes from the local `main` branch to the `main` branch of the forked repo at your GitHub account.

```bash
$ git add .
$ git commit -m "Your note"
$ git push origin main
```

You will then resume the process at step 6 to submit a pull request.

If you plan to continue working locally and submitting pull requests, you may want to add an upstream remote locally that points to the /dev/mtl repo, in order to fetch changes. You may also want to consider creating a feature branch (also known as a "topic" branch), making your changes there (instead of in the `main` branch), pushing to GitHub and submitting the update via pull request. You can then keep your `main` branch up-to-date while working on multiple features.

## License

[MIT License](LICENSE)
