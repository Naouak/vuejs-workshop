# vuejs-workshop

> Material for a Vue.js workshop I organize.

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).

## List of exercises :

1. Create a component `Question` and use it in App.vue
2. Add a required parameter `question` to `Question` and pass a text from App.vue to `Question`.
3. Use `v-for` to create a list of `Question` from an array in data.
4. Use the array key to show the question number.
5. Add a `Choice` component that would show a possible answer in a `Question`.
Each answer should be provided by App.vue to `Question` then to `Choice`.