# WebPackage
WebPackage is a *revolutionary* new way of distributing web apps on any platform. It works by packaging the web app in a `.webpkg` file, a special kind of zip file designed for distributing web apps. 
## Use Cases
* In third-world countries, web apps and games can be distributed P2P and run in any client that reads these packages
## WebPackage vs. PWA
* put something here
## Client Specifications
For a webpackage client to function it must be able to  
* Import a .webpkg by extracting the file in the same manor as a .zip and place the .web  in an appropriate directory  
* Export a .webpkg by removing local-package.json and then zipping the .web and naming it with a .webpkg extension  
* Render a full html5 and javascript local webpage from the .web directory  
* If required, save client specific metadata in local-package.json  
## Package Structure
The structure of a `.webpkg` contains a folder named the id of the app with .web at the end and contains two folders, a `app` folder and a `meta` folder. The `app` folder is where you store all of the code, such as html, css, and javascript files. The `meta` folder is where you store an icon and a `package.json` file. `local-package.json` is where the client stores user specific information that would not make sense to be distributed and its contents is specific to the client and should not be included in a release.  
general layout:  
```
id.webpkg  
|- id.web/  
|-- meta/  
|--- package.json  
|--- local-package.json  
|--- icon.png  
|-- app/  
|--- index.html  
|--- ...  
```
### package.json
a general layout of the `package.json`:
```json
{
  "id": "foo",
  "title": "bar",
  "author": "John Doe",
  "version": "1.0",
  "icon": "icon.png"
}
```
