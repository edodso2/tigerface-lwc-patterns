# Tigerface Systems LWC Patterns

LWC (lightning web component) coding patterns unique to Tigerface Systems that can be referenced in code comments. This is so that explanations for unique patterns do not have to be explained in the code and can simply link to this readme.

## 1. Static Class List Variables

Use static variables for class lists. This is only helpful if you plan to write a JEST test for the component or you repeat the class names multiple times in the component. In the JEST test you can use these static variables instead of having to redefine them for assertions.

```JavaScript
export default class Component extends LightningElement {
  /**
   * Static class list variables
   * See pattern 1
   */
  static defaultClassList = 'my-component-class';
  static visibleClassList = 'my-component-class-visible';
}
```

