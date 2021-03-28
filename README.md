# Dynamically Adaptive Navbar

With this thing you can create a navbar which items will always fit to the screen size. It has no styles but a predefined structure, basicaly it`s just a structured sceleton with a provided js functionality so you can decorate it by your taste

### The build contains:
- **nav.html** - (html sceleton)
- **nav-blanc.scss** - (all class names without styles)
- **nav-default.scss** - (basic styles to shape things up)
- **nav.js** - all functionality

# How to use it

## Markup and styles
So you can write all styles completely by yourself using a blank file with all class names - **nav-blanc.scss** or the way a recommend to do this - use only **nav-default.scss** and write your styles right into it. Following this way, in most cases, you will only need to set up a font properties, some paddings and margins and will get a fully responsive navbar, also some media queries were added already

## Adding functionality
at first you ned to create a navbar instance and give it your navbar's class name

```js
let topmenu = new Nav('topmenu');
```
that provides click functionality to navbar's buttons like menu icon (you can see it only on screens under 920px) and expand-menu icon (it appears on a defined breakpoints).  

## Adding adaptivity
The way it works is you just set a number of elements that should be visible under specific breakpont.  
```js
topmenu.setItemsOnBreakpoint(3, 1200);
```
Breakpoints are defined as mobile first so the example abow will make only 3 items visible and hide all others until the screen will reach 1200px width  
You can define multiple breakpoints by this way
```js
topmenu.setItemsOnBreakpoint(3, 1200);
topmenu.setItemsOnBreakpoint(2, 1100);
topmenu.setItemsOnBreakpoint(null, 920);
```
if the number of items is setted as `null` all items will be visible

