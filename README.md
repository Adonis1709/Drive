
### 🌙 Dark Mode is here!

As of `v.conscious-club/0.2.0`, the app will automatically adjust to your OS's dark mode settings.

![darkmodedemo](static/gd_darkmode_demo.gif)

## 📀 Installation

### Release page

### For MacOS/Linux users with Homebrew + Homebrew Cask

This method is highly recommended for users who want the latest release without the hassle of downloading the executable each time. Learn more about how to get [`homebrew`](https://brew.sh/) and [`homebrew-cask`](https://github.com/Homebrew/homebrew-cask).

The following script will install `G Desktop Suite.app` into your `Applications/` folder.

```sh
brew cask install g-desktop-suite
```

Run `brew cask upgrade` to get the latest version of the app.

### For Arch Linux and related distributions

Install the AUR package [`g-desktop-suite-git`](https://aur.archlinux.org/packages/g-desktop-suite-git/). Below is an example with [`yay`](https://github.com/Jguer/yay), but any AUR manager will work.

```sh
yay -S g-desktop-suite-git
```

## 📸 Action Shots

![two-window](static/two-window-shot.png)

![dark-shot](static/dark-shot.png)

## ✏️ Development

To build the app locally, clone the repository, install all dependencies, and run the available npm scripts.

```sh
git clone https://github.com/Adonis1709/Drive.git
cd G-Desktop-Suite
yarn install
```

```sh
$ yarn run
yarn run v1.22.4
   - build
      electron-builder -mwl -p never
   - build-cask
      ./Casks/update.sh $npm_package_version
   - clean
      concurrently "prettier './**/*.js' --write" "eslint ./**/*.js --fix"
   - clean-check
      concurrently "prettier './**/*.js' --list-different" "eslint ./**/*.js"
   - deploy
      electron-builder -mwl -p onTagOrDraft
   - deploy-cask
      cask-repair g-desktop-suite -v $npm_package_version -b
   - dev
      cross-env NODE_ENV=development electron .
   - pack
      electron-builder --dir && yarn update-cask
   - start
      electron .
```

To build production ready applications for macos (dmg), windows (exe), and linux (sh), run `yarn build`.

🛎️ **Have suggestions?** Feel free to create an issue or make a pull request.

🤝 **Want to contribute?** Check out the `TODO.md`!

### Dependencies

- [about-window](https://ghub.io/about-window): &#39;About App&#39; window for Electron application
- [electron-localshortcut](https://ghub.io/electron-localshortcut): register/unregister a keyboard shortcut locally to a BrowserWindow instance, without using a Menu
- [electron-window-state](https://ghub.io/electron-window-state): Simple module that helps to save and restore size and position of Electron windows.
- [file-system](https://ghub.io/file-system): Strengthen the ability of file system

### Dev Dependencies

- [cross-env](https://ghub.io/cross-env): Run scripts that set and use environment variables across platforms
- [del](https://ghub.io/del): Delete files and directories
- [electron](https://ghub.io/electron): Build cross platform desktop apps with JavaScript, HTML, and CSS
- [electron-packager](https://ghub.io/electron-packager): Customize and package your Electron app with OS-specific bundles (.app, .exe, etc.) via JS or CLI

## 📜 MIT License

_Disclaimer: Not affiliated with Google._
