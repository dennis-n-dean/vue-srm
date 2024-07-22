# Vue SRM

> A lightweight Source Relationship Management (SRM) system for collaborative journalism.

The goal of this project is to create a simple, easy-to-use shared repository for collaborative newsrooms to share source contact information and background knowledge.


#### Features

* This project is built from Vue 2 PWA template by default.
* The UI part is built on the top of Vuetify.
* It inlcudes Vuex and Axios to manage authentication.
* The dashboard uses vue-chartjs to create charts on dashboard.
* The project is built on TypeScript.

## Build Setup

``` bash

# Clone project
git clone https://github.com/dennis-n-dean/vue-srm.git


# install dependences
cd vue-srm
npm install --from-lock-file

# or use yarn
npm install -g yarn
yarn

# serve with hot reload at localhost:8080
npm run start


## You will see the following output. You can test API with the URLs via browser.
##[1]
##[1] > vue2crm@1.2.0 start <your_path>\vue2crm
##[1] > node build/dev-server.js
##[1] > Starting dev server...
##[1]  DONE  Compiled successfully in xx:xx:xx
##[1]
##[1] > Listening at http://localhost:8080

# Visit the app at [http://localhost:8080](http://localhost:8080)

```

## Docker 


```bash
## Run / Test release without building new image
npm run build

# Launch nginx image to test latest release
docker pull nginx:alpine
docker run -p 8080:80 -v \
    <your_aboslute_path>/dist:/usr/share/nginx/html nginx:alpine


# Build release image
docker build . -t  vc-prd:2.0

# Launch the development image in the backgroud
docker run --rm -d --publish 8080:80  --name vc2 vc-prd:2.0

# Check the log
docker logs vc2   -f

```


For detailed explanation on how things work, checkout following links

* [vuex](https://vuex.vuejs.org/en/)
* [vuetify](https://vuetifyjs.com/)
* [axios](https://github.com/mzabriskie/axios/)
* [vue-chartjs](https://github.com/apertureless/vue-chartjs)
* [vue-progressbar](https://github.com/hilongjw/vue-progressbar)
* [webpack guide](http://vuejs-templates.github.io/webpack/)
* [vue-loader](http://vuejs.github.io/vue-loader).

