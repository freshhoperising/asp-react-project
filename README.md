# AspNetReactSamples

Welcome to this ASP.NET solution which contains examples of how to incorporate, build and Unit Test 
[React](https://facebook.github.io/react/) front-end inside an ASP.NET Core (1.0.0) and ASP.NET MVC5 
application. 

## Using these templates to create your own React.js application

If you want to create your own ASP.NET application that runs a React.js application then 
it is fairly easy to copy a few files from these sample projects to add React.js 
build and run capabilites.

## NOTE: Making the application ready for production

While the React build process have totally valid development and production
paths I haven't handled all the ASP.NET side of production/deployment. 
Things that would need to be added:

- I have set up cachebuster values to ReactWebPack.Core in production mode
but I haven't done anything in the ReactWebPack.MVC5 project. 
- I have changed the endings of the `vendor.js` and `main.js` to ...**min**.js
in ReactWebPack.Core, but not in ReactWebPack.MVC5.
- The ASP.NET Core project now uses the VS2017
[bundle and minifier extension](https://visualstudiogallery.msdn.microsoft.com/9ec27da7-e24b-4d56-8064-fd7e88ac1c40)
instead of Gulp. I have minified the CSS files using this extension so there should be no need to run it again.