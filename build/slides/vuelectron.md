<!-- .slide: data-state="title" -->

![Electron](./images/electron.svg)<!-- .slide: data-state="title" --> ![Vuejs](./images/vuejs.svg)

# Electron/Vue Fusion

Creating Desktop Apps with Electron and the Vue.js Framework

<div class="small mt-4"><span class="badge badge-light mr-1 ml-2">&larr; &rarr;</span> navigate
<span class="badge badge-light mr-1 ml-2">t</span>toolbar
<span class="badge badge-light mr-1 ml-2">m</span>menu
<span class="badge badge-light mr-1 ml-2">esc</span>overview</div>

---

# Who am I?

- [Staff Author](https://www.linkedin.com/learning/instructors/ray-villalobos?u=104) (Lynda/LiL)
- Get it Free:<br>
  [Seminole](http://www.seminolecountyfl.gov/departments-services/leisure-services/seminole-county-library), [Osceola](http://www.myosceolalibrary.org)<br>
  [Orange](https://www.ocls.info), [Volusia](http://volusialibrary.org), [Veterans](https://linkedinforgood.linkedin.com/programs/veterans)

---

![Electron](./images/electron.svg)
# What is Electron?
- CSS, HTML & JS Apps
- Node.js & Chromium V8
- Menus, Windows, APIs

---

# Who Uses it?
- [Atom](https://atom.io/), [VS Code](https://code.visualstudio.com/), [Slack](https://slack.com/), [Teams](https://products.office.com/en-US/microsoft-teams/group-chat-software)<br> [Discord](https://discordapp.com/), [Hyper](https://hyper.is/), [Notion](https://www.notion.so/)<br>[Figma](https://www.figma.com/), [Twitch](https://www.twitch.tv/downloads)<br>[WhatsApp](https://www.whatsapp.com/), [Skype](https://www.skype.com/en/), <br>[Bootstrap Studio](https://bootstrapstudio.io/), [Notable](https://github.com/notable/notable)
- [More](https://electronjs.org/apps)

---

# Advantages/Disadvantages
1. Leverage your skills
1. Node Modules
1. Easy to update
1. Large Files
1. Non Native

---
![Vuejs](./images/vuejs.svg)

# Why Vue?
1. Reactive
1. Virtual DOM
1. Components

---

<!-- .slide: data-state="title" -->
# Easy to add
---

<!-- .slide: data-state="textonimage" data-background-image="http://pixelprowess.com/i/includingvue.svg" -->

---

# Vue Basics <a class="btn btn-danger btn-lg text-white" href="https://codepen.io/planetoftheweb/pen/oJOwYb"><i class="fab fa-codepen"></i></a>
- DOM Target
- `Vue({})` Object
- `data: {}`
- `Try It` Add data, app.name

---

# Template Directives  <a class="btn btn-danger btn-lg text-white" href="https://codepen.io/planetoftheweb/pen/BMyKyw?editors=1010"><i class="fab fa-codepen"></i></a>

- `v-for`
- `v-if`
- `Try it`: Change maximum, add a product

---

# Reactive data <a class="btn btn-danger btn-lg text-white" href="https://codepen.io/planetoftheweb/pen/OYwwJZ?editors=1010"><i class="fab fa-codepen"></i></a>

- `v-model`
- `mounted` lifecycle hook
- No event tracking
- `Try it`: Add a minimum


---

# Events <a class="btn btn-danger btn-lg text-white" href="https://codepen.io/planetoftheweb/pen/yZJZQM?editors=1010"><i class="fab fa-codepen"></i></a>

- `v-on`
- `methods` object
- `Try it`: Removing an item

---

# Finished Codepen <a class="btn btn-danger btn-lg text-white" href="https://codepen.io/planetoftheweb/pen/omWNQd?editors=1010"><i class="fab fa-codepen"></i></a>


- Filters
- Computed Properties
- Animation

---
# Finished Course <a class="btn btn-primary btn-lg text-white fab fa-linkedin-in" href="https://www.linkedin.com/learning/vue-js-essential-training-2"></a> <a class="btn btn-success btn-lg text-white fab fa-github-alt" href="https://github.com/planetoftheweb/vue-essentials"></a>

- Vue CLI
- Routing


---
<!-- .slide: data-state="title" -->

<i class="fab fa-github-alt" style="font-size: 5rem;"></i>
# Git Interlude

---

# Download All Branches

```
mkdir electronvue
cd electronvue
git clone --bare https://github.com/planetoftheweb/electron-4 .git (make sure you add extra .git)
git config --bool core.bare false
git reset --hard
```

---

# Getting ready

- `npm install`
- git stash (pop)
- git diff (difftool)

---
<!-- .slide: data-state="title" -->
![Electron](./images/electron.svg)

# Electron Essentials

---

# Installing Electron

```
npm i -D electron@beta
```

- [Many versions](https://electronjs.org/)
- NodeJS
- Chromium

---

# Your First App

- `mkdir yourapp`
- `npm i -y`
- `npm i --save-dev electron@4.1.4`


---

# index.js

```
const { app, BrowserWindow } = require('electron');

function createWindows() {
  let appWindow = new BrowserWindow();
  appWindow.loadURL('https://7ty.tech');
}

app.on('ready', createWindows);
```

---

# Important Concepts

- `app`
- `BrowserWindow`
- `app.on('ready', function)`
- [Docs](https://electronjs.org/docs)

---

# Files not URLs <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/01_03b...01_03e"><i class="fab fa-github-alt"></i></a>

- Loads doc from the root
- [loadFile()](https://electronjs.org/docs/api/web-contents#contentsloadfilefilepath-options)

---

# BrowserWindow <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/02_01b...02_01e"><i class="fab fa-github-alt"></i></a>

- [Tons of Options](https://electronjs.org/docs/api/browser-window)
- Size, frame, opened

---

# AppWindow <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/02_02b...02_02e"><i class="fab fa-github-alt"></i></a>

- `git stash && git checkout 02_02e`
- `show: false`
- `.on('closed')`
- `.once('ready-to-show')`

---

# Managing Windows <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/02_03b...02_03e"><i class="fab fa-github-alt"></i></a>

- `frame`

---

# Inter Window Communication <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/02_04b...02_04e"><i class="fab fa-github-alt"></i></a>

- `.hide`
- Frameless Windows

---

# IPC <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/02_05b...02_05e"><i class="fab fa-github-alt"></i></a>
- Inter Process Communication
- `ipcMain`
- `ipcRenderer`

---
<!-- .slide: data-state="title" -->

# Vue Fusion

---

# CLI & Builder

- [Vue CLI](https://cli.vuejs.org/)
- Prebuilt process, Live Reload


---
# Vue CLI Install

```
npm install -g @vue/cli
vue create electron-new
## winpty vue.cmd create electron-new
## Gitbash PC
cd electron-new
npm run serve
```
---
<!-- .slide: data-state="title" -->

# Explore Installation

---

# Electron Builder plugin

- [Electron Builder](https://nklayman.github.io/vue-cli-plugin-electron-builder/)
- Debugging Default
- `npm run electron:serve`
- `main.js`

---

# Incorporating Vue Project

- Copying an Existing Project
- `git stash && git checkout 03_02e`
- Installing Additional Packages

---

# Menus <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/05_01b...05_01e"><i class="fab fa-github-alt"></i></a>

- [Menu class](https://electronjs.org/docs/api/menu)

---

# IPC in Menus <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/05_02b...05_02e"><i class="fab fa-github-alt"></i></a>

- [Menu class](https://electronjs.org/docs/api/menu)

```
accelerator: process.platform === 'darwin' ? "Command+shift+I" : "Ctrl+shift+I",
click(item) {
  win.webContents.send("shop");
}
```

---
# Icons <a class="btn btn-primary text-white" href="https://github.com/planetoftheweb/electron-4/compare/05_03b...05_03e"><i class="fab fa-github-alt"></i></a>

- Part of Window object


---

<!-- .slide: data-state="title" -->
The End
