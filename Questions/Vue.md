# Vue Questions.

## 1. Explain the differences between one-way data flow and two-way data binding?

By definition, one-way data flow means that the model is the only source of truth. While two-way data-binding means that UI fields are found to model data. Therefore, in case UI field changes, the model data also changes and vice-versa.

Secondly, one-way data flows are deterministic, in contrast, the two-way binding is associated with several side effects that are difficult to identify and understand.

Additionally, for one-way data flow, the UI aspect of the application can not update automatically. This, in turn, results in a need to customize certain codes to help it update every time there is a change in the data model. Whereas, in data binding, the UI part of the application usually updates automatically when the data model is changed.

**Note:**  
You want to hear that the candidate is aware of the v-model directive, and bonus points if they are able to describe what v-model does under the hood. Also good to hear the candidate is aware that props are one-way binding.

---

## 2. List some of the component lifecycle hooks that are available in Vue.js.

A list of most of the lifecycle hooks that are available in Vue:

| Hook | Description |
| --- | --- |
| `beforeCreate` | It is called immediately after the instance has been initialized and before that all the options will be processed. |
| `created` | It is called right after the instance has been created and all the options have been set up. |
| `beforeMount` | It is called right before the mounting of the DOM begins. |
| `mounted` | It is called when the instance has been mounted and the el(the DOM) has been replaced. |
| `beforeUpdate` | It is called when some data changes and before the DOM has been re-rendered. |
| `updated` | It is called when some data changed and the DOM has been re-rendered. |
| `activated` | This hook is used for `<keep-alive>` components (You can read more about it here), it allows you to know when a component inside the `<keep-alive></keep-alive>` tag is toggled ON. |
| `deactivated` | This hook is used also for `<keep-alive>` components, it allows you to know when a component inside the `<keep-alive></keep-alive>` tag is toggled OFF. |
| `beforeDestroy` | It is called right before the Vue instance is destroyed. At this stage the instance is still fully functional. |
| `destroyed` | It is called after the Vue instance has been destroyed, this doesn’t mean that it will remove all the code from the DOM but that it will remove all the Java Script logic and the instance will not exist anymore. |
| `errorCaptured` | Called when an error from any descendent component is captured. The hook receives three arguments: the error, the component instance that triggered the error, and a string containing information on where the error was captured. The hook can return false to stop the error from propagating further. |

**Note:**  
Good to hear they understand created, mounted and beforeDestroy lifecycle hooks, these are the most commonly used, others are a bonis, and big bonus points for knowing about the errorCaptured hook.

---

## 3. Why should arrow functions not be used while writing lifecycle hooks in Vue instance?

Arrow functions are not independent, as a result, they cannot define a `this` of their own. But instead, the arrow functions are bound to their parent’s function’s context.

In a situation where the arrow function (`=>`) is used in the Vue app, the keyword ‘this’ does not bind to the Vue instance and therefore, resulting in errors.

For that reason, it is highly advised to use the standard function declaration instead of the arrow function.

**Note:**  
This is a well known thing in the Vue community, and if they are not aware of it then that is a red flag, bonus points if they suggest it can sometimes be useful - like when Vue is initialised inside of another class in more custom environments.

---

## 4. In Vue 2.x, explain reactivity and common issues when tracking changes?

Generally, this is a very common Vue interview question. Usually, all properties defined in Vue instance are very reactive. This means that in case of any change, the components automatically update and re-render.

Therefore, all these properties are changed to getters and setters in the inItialization stage. Hence, giving Vue the ability to detect when these properties are changed.

Above all, the following setbacks must be considered while designing a Vue app;

Because of JavaScript limitation, Vue cannot detect the deletion or addition of an object property.
Additionally, it cannot also detect the modification of array items, hence, the need to use Vue .set.

**Note:**  
You could probe them about Vue 3 (if they know it), which uses the new Proxy class to detect changes, which fixes the above issues.

---

## 5. What are mixins? Briefly describe their advantages and disadvantages.

Mixins are flexible methods of redistributing reusable features for Vue components. A mixin object can accommodate any component option. When a component uses a mixin, all mixin components are merged with components options.

Advantages of using:
- It has several objects for heap allocation.
- It’s run time assembly can prevent the problem of supporting persistence.
- Additionally, the run time assembly can also lead to objects which seem mysterious.

Disadvantages of using mixins
- It increases dependencies.
- Global mixins affect every component, hence this can result in a serious maintenance problem.

In Vue 3, mixins are no longer supported, they do exist still and can be done using a variety of ways, but they are not recommended.

**Note:**  
Good to hear that they understand mixins, and that they are not recommended, but if they can give a good example of using them, that is a big bonus point - but not required if not.

---

## 6. State some features of Vue.js?

Vue.js have the following features;

- It has a Virtual DOM.
- It has a data-binding feature which helps in manipulating values to HTML attributes.
- Its components help in creating customized components that are in turn used in HTML.
- The capability of providing a transition to HTML elements.
- Vue.js has HTML based templates.
- Built-in directives such as v-show.
- It has watchers which are applied to data that changes.
- Vue. j’s is a lightweight thus better performance.
- Routing feature which makes it possible to navigate between pages.

**Note:**  
Not really a requirement, but good to hear that they know about these features specifically.

---

## 7. Which lifecycle hook is best for collecting data from API calls?

This mainly depends on its usage and the purpose of the component. Usually, the newly `created` lifecycle hook is normally the best for placing an API call. This is because, at this stage, the reactivity features and component data are available to operate despite the fact that the components haven’t rendered yet.

**Note:**  
It's usually good practice to use the created lifecycle hook for API calls, but you can use the `mounted` one as well.

---

## 8. What is Virtual Dom and what are some of its benefits?

The main use of Virtual DOM to quickly and efficiently manipulate the DOM. In a situation where there are several nodes in the DOM, the updating process is very expensive due to resources required and processing power.

Using the virtual DOM JavaScript object is preferably faster and very efficient. Lastly, Vue.js automatically organizes DOM updates in batches, therefore, boosting efficiency.

**Note:**  
A key understanding from the candidate is that it is a tree type structure that is used to represent the DOM.
