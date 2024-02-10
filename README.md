# vue-basics

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

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


### Purposes of this project
Learning Vuejs from Nutshell

### Vue3 Migration Guide
See [Filters](https://v3-migration.vuejs.org/breaking-changes/filters.html)

### Concepts
- 2ways binding
- LifeCycle
  - [lifecycle hook](https://vuejs.org/guide/essentials/lifecycle.html)

- Binding:
  value binding
  property binding:
    v-bind:[property name]

- Model: Link element with property
  v-model

- Event handling:
  - Catch events from elements:
    ```
    v-on:event => @event="{function()}"
    ```
- Prevent default event
  - Cancel default event of this element

- ref: 
  - Refer to element

- conditional rendering: 
  ```
  v-show, v-hide, v-if, v-else-if, v-else
  ```

- List rendering: 
  ```
  v-for
  ```

- Methods: 
  - functions of vue object

- Watch: 
  - tracking changes of data

- Hooks:
  - mounted()

- props:
  - Convey data from parent comp to child comp
  - dynamic and static props

- filters:
  - format data before rendering 
  - local and global filters
