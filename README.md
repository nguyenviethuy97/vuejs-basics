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

### Differences between Composition and Option API
See [Diff](https://www.linkedin.com/pulse/vue-3-options-api-vs-composition-whats-difference-md-najmul-hasan/)

### Concepts
- 2ways binding
- LifeCycle
  - [lifecycle hook](https://vuejs.org/guide/essentials/lifecycle.html)
  - [created() hook](https://vuejs.org/api/options-lifecycle.html#created)
    - Called after the instance has finished processing all state-related options.
    
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
  - [props doc](https://vuejs.org/guide/components/props.html)
  - Convey data from parent comp to child comp
  - Props are read only
  - dynamic and static props
  - How to change props from child comp: using event function in props 
  ```html
  <child-comp :change-prop-event="(value) => prop = value"><child-comp>
  ```

- filters:
  - format data before rendering 
  - local and global filters

- compute properties
  - A computed property automatically tracks its reactive dependencies. Vue is aware that the computation of computed functions depends on state or ever value, so it will update any bindings that depend on compute function when state changes.