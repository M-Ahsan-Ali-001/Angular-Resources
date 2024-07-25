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
