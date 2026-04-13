### Prerequisites
- Ruby (recommended via Homebrew on macOS)
- Bundler

### First-time setup

macOS (zsh):
```bash
xcode-select --install
brew install ruby@3.2
gem install bundler
# Add path to shell config
echo 'export PATH="/opt/homebrew/opt/ruby@3.2/bin:$PATH"' >> ~/.zshrc
# Reload 
source ~/.zshrc
# Then restart computer to clear xcode cache
```

Windows (PowerShell):
Install `ruby_devkit 3.4.x` from ([https://rubyinstaller.org/downloads/](https://rubyinstaller.org/downloads/)), ensure MSYS2 is also installed
In the powershell, install the packages. Then `cd` to your repo, where there should be a file called `Gemfile`, and install it
```powershell
gem install bundler jekyll
```

### Setup
 `cd` to your repo, where there should be a file called `Gemfile`, and install it
```powershell
cd /path/to/my/repo
bundle install
```

### Run locally
```bash
bundle exec jekyll serve --livereload
```


Then open the local path, which is the following by default:

- http://127.0.0.1:4000


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

### 7) Mac permission error when trying to use the `gem install bundler` command
You need sudo to fix the ownership first:
- Give yourself ownership of the file:
```bash
sudo chown {insert your user account here} ~/.zshrc
```

- Now add write permission:
```bash
chmod u+w ~/.zshrc
```
- Then add the PATH line:
```bash
echo 'export PATH="/opt/homebrew/opt/ruby@3.2/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```
- Verify Ruby:
```bash
which ruby
```
- Install bundler:
```bash
gem install bundler
```