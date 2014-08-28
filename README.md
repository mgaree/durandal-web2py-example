This web2py appliance provides the DurandalJS 'Get Started' tutorial 
(http://durandaljs.com/get-started.html). The only differences between the code
here and in the tutorial are in the file paths.

In a typical DurandalJS app, /app and /lib are in the root folder. However,
/app and /lib can't be served from the /views folder by web2py (since they're 
not controller functions), so I moved those to /static and changed the data 
source `data-main` in the view. 

Separate folders within /static/app can be used to allow multiple controllers 
to use DurandalJS. Naming the main js file `main.js` is not required, so multiple
controller functions can be supported within a single folder. 

Improvements that should be made to this example include:
- moving the css/js includes from the view (index.html) to the layout file
- using css to prevent the Durandal navigation bar from obscuring the web2py navigation bar
- implementing the UI improvements found in the Durandal HTML Starter Kit