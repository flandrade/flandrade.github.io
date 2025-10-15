# flandrade.github.io

Personal website

[![CircleCI](https://circleci.com/gh/flandrade/flandrade.github.io.svg?style=svg)](https://circleci.com/gh/flandrade/flandrade.github.io)

## 🚀 Get Started

### Prerequisites

Install [asdf] and [asdf-ruby] to manage Ruby versions:

```bash
# Install asdf (if not already installed)
brew install asdf

# Add asdf to your shell (add to ~/.zshrc for persistence)
echo -e "\n. $(brew --prefix asdf)/libexec/asdf.sh" >> ~/.zshrc
source ~/.zshrc

# Install Ruby plugin
asdf plugin add ruby
```

### Installation

Clone this repository to your local drive:

```bash
git clone git@github.com:flandrade/flandrade.github.io.git
cd flandrade.github.io
```

Install Ruby with asdf:

```bash
asdf install ruby 3.1.4
```

Install Bundler and Jekyll dependencies:

```bash
gem install bundler
bundle install
```

### Running Locally

Build the site and make it available on a local server:

```bash
bundle exec jekyll serve
```

Then open http://localhost:4000 in your browser.

[asdf]: https://asdf-vm.com/
[asdf-ruby]: https://github.com/asdf-vm/asdf-ruby
