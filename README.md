# dashboard-app

## About

Dashboard App with contact information and calendar, easily accessible by sidebar navigation

Since the short time to complete the app, I decided to use an UI framework to be faster and the choosen one was Vuetify

### Why Vuetify

Vuetify provide developers with the tools they need to build rich and engaging user experiences. Unlike other frameworks, Vuetify is designed from the ground up to be easy to learn and rewarding to master with hundreds of carefully crafted components from the Material Design specification 

## Steps followed

- create the app with vue create dashboard-app
- vuetify with vue add vuetify
- when adding vuetify, it also adds sass so no need to also install that in the project (it was my purpose to use sass in this project)
- create github repo and push project (easy todo explanation can be found here: [How to add an existing project to GitHub – using the command line](https://dev.to/monicafidalgo/how-to-add-an-existing-project-to-github-using-the-command-line-27n9))
- divide folders by components
- for the sidebar navigation icons, I inspected the figma file and checked the icon name, since the design seems to use material design I looked up into [material design icons](https://materialdesignicons.com/) and searched for dashboard. Later I read the vuetify docs in how to use them, it needs the mdi- prefix followed by the icon name
- imported the google font, Poppins and add it has the project new font-family
- added the calendar, table and footer components
- created the data for each component
- implemented the [ITCSS folder scructure](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/)

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```
