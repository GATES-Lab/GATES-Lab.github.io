# GATES-Lab.github.io
Repo hosting the website of the GATES-Lab project.

## Local development

This site is built with Jekyll (GitHub Pages configuration).

### Prerequisites
- Ruby (recommended via Homebrew on macOS)
- Bundler

### First-time setup (copy/paste)

macOS (zsh):
```bash
xcode-select --install
brew install ruby
gem install bundler
bundle install
bundle exec jekyll serve --livereload
```

Windows (PowerShell):
```powershell
# Install Ruby with RubyInstaller + MSYS2 first, then restart PowerShell
gem install bundler
bundle install
bundle exec jekyll serve --livereload
```

Then open:

- http://127.0.0.1:4000

### Setup
```bash
bundle install
```

### Run locally
```bash
bundle exec jekyll serve --livereload
```

### Notes
- If `bundle` is not found, install it with:
```bash
gem install bundler
```

## Troubleshooting (macOS and Windows)

### 1) `bundle install` fails
- macOS: ensure Xcode Command Line Tools are installed: `xcode-select --install`
- macOS: if Ruby is missing/outdated, install with Homebrew: `brew install ruby`
- Windows: install Ruby via RubyInstaller (with MSYS2) and reopen terminal

### 2) `bundle` command is not found after install
- macOS: restart terminal so PATH updates are applied
- Windows PowerShell: restart terminal after Ruby/Bundler install
- Run: `gem install bundler`

### 3) Jekyll fails with missing gems
- Run: `bundle install`
- Then run with Bundler prefix: `bundle exec jekyll serve --livereload`

### 4) Server starts but page does not load
- Open: http://127.0.0.1:4000
- If port 4000 is busy, run: `bundle exec jekyll serve --livereload --port 4001`

### 5) Theme or content changes are not appearing
- Stop server and restart: `bundle exec jekyll serve --livereload`
- If needed, clean generated files: `bundle exec jekyll clean`

### 6) Windows line-ending issues
- If commits show large markdown diffs, configure Git line endings for your setup:
	- Windows typical: `git config --global core.autocrlf true`
	- macOS typical: `git config --global core.autocrlf input`
