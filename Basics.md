# Interface
~~~
interface ObjectR{
[key : string] :any;

}
// work like objects in JS but type is strict
~~~

# Simple Class and Functions
~~~
export class CoursesComponent {
  list = ["gogle", "fox", "Nmap"];
  dict:ObjectR = {
    "gogle": 0,
    "fox": 1,
    "Nmap": 2
  };
  dictKeys: string[] = [];

  x:any;

  constructor() {
    // Get the keys of the dict object and store them in dictKeys array
    this.dictKeys = Object.keys(this.dict);
  this.x =9;
  }

  func(item: string) {
    return `${item}`;
  }

  OnClick(key:string) {
    alert(this.dict[key]);

  }
}


~~~


# Components
~~~

@Component({
  selector: 'courses',
  template: `
    <div *ngFor="let key of dictKeys">
      <h2 (click)="OnClick(key)">{{ func(key) }}</h2>
    </div>
  `
})
~~~



# Create a Service
~~~
// A service is an Angular Component for creating  Components that can be used by angular files using dependency injection
// create a new file with a name and extension like comp.service.ts
// import the service to the app.modules.ts in provider array
//simple export class is used.
// try to access the srevice using  class constructure it avoid coupling issues and best fot unit testing

~~~

# Angular Built-In Animation
~~~
@Component({
  selector: 'MainBody',
  templateUrl: './mainnbody.component.html',
  styleUrls: ['./mainnbody.component.css'], 
  animations: [
    trigger('fadeAnimation', [
     
      state('hidden', style({ opacity: 0 })),
      state('visible', style({ opacity: 1 })),
      transition('visible => hidden', [
        animate('500ms ease-out')
      ]),
      transition('hidden => visible', [
        animate('500ms ease-out')
      ]),
    ])
  ]
})

// developer can use these animation functions to create animations
~~~

# Directives
~~~
Some of the most common structural directives are:

`*ngIf`: This directive conditionally renders an element based on an expression.
`*ngFor`: This directive iterates over an array and renders an element for each item in the array.
`*ngSwitch`: This directive renders different elements based on the value of an expression.

Some of the most common attribute directives are:

`ngClass`: This directive adds or removes CSS classes based on an expression.
`ngStyle`: This directive sets CSS properties based on an expression.
`ngClick`: This directive listens for a click event and executes a function.
~~~
