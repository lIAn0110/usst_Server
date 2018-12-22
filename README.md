# this is a template

> A project template with mpvue+iView

# Install it
### First: you must insure you alredy install npm\vue enviroment

### clone mpvue Codes
``` bash
## `getStart` is your project name
git clone https://github.com/gitcyc/mpvue getStart
``` 

### clone iView Codes
``` bash
git clone https://github.com/TalkingData/iview-weapp
# [cmd] move the core codes to your project
move iview-weapp/dist getStart/dist/static/iview
# [cmd] delete the others file
rmdir /s/q iview-weapp
``` 

### install dependencies
``` bash
cd getStart
npm install
```

### Compiling and work
``` bash
npm run dev
```

### Other command
``` bash

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

### notice
##### if you want to modify the config of compile option, try to modify these two files:package.json、config/index.js

### MORE

Guide (http://vuejs-templates.github.io/webpack/)

Docs (http://vuejs.github.io/vue-loader)

