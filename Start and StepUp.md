# Create New Project
~~~
ng new projectname #for standalone project (no NG Module ....)
ng new projectname --no-standalone
~~~

# Start the server

~~~
ng serve
~~~

# Create a New Component

~~~
ng g c ComponentName
~~~


# Add a component manually
~~~

1) Add a new file with nameand extension  like "name.component.ts" and export the component
2) go to app.module.ts and import the component 
3) add the imported module name to decalaration.
4) remove and addd your content to app.component.html
~~~

# Create a new service

~~~
ng g s nameservice
// it allow data to be shared with all the available modules
~~~
