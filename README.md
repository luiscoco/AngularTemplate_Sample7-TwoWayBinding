# two-way-binding

In Angular, two-way binding is a feature that allows synchronization of data between a component and its template in both directions. It means that changes made to the data in the component will reflect in the template, and vice versa.

Two-way binding is denoted by the [(ngModel)] directive, which combines property binding and event binding into a single syntax. It is commonly used with form elements such as input fields, checkboxes, and selects.

Here's a simple example to illustrate two-way binding in Angular:

HTML Template:
```typescript
<input [(ngModel)]="name" placeholder="Enter your name">
<p>Hello, {{ name }}!</p>
```

Component:
```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-example',
  templateUrl: './example.component.html',
  styleUrls: ['./example.component.css']
})
export class ExampleComponent {
  name: string = 'John Doe';
}
```

In this example, we have an input field with the [(ngModel)] directive bound to the name property of the component. Whatever value is entered in the input field will be automatically updated in the name property. Similarly, any changes made to the name property in the component will be reflected in the template.

The paragraph tag below the input field displays the greeting message with the value of name using interpolation ({{ name }}). Whenever the value of name changes, the greeting message will be automatically updated in the template.

This two-way binding ensures that the data in the component and the template are always in sync, simplifying the process of handling user input and displaying dynamic data.


