# VueJs Components Communication

> A simple app to show how parent-child communication within Vuejs app takes place.

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev --watch

# build for production with minification
npm run build
```

## Releases/Progress
This is a breakdown of progress from the initial commit to attaining the goal of this tutorial. 
The progress has been tagged and you can switch between the "releases".

 * v1.0.2
    - Implemented Child-Parent communication
      - Emitting event from ChildOne to parent.
      - Receiving the event and updating local variable.
  * v1.0.1
    - Added Twitter Bootstrap cdn link
    - Added components 
      - Created components folder and added 3 components.
    - Implemented Parent-Child communication. 
      - Passing message from Parent component to ChildOne, ChildTwo and ChildThree
      - Dynamically changing message in Child 2 from parent
  * v1.0.0
    - Initial commit of the webpack-simple template

## The Big Picture
![Screenshot 1](https://github.com/lawrence615/component-communication/blob/master/big-picture.png)

