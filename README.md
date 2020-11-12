# WebPackage
WebPackage is a *revolutionary* new way of distributing web apps on any platform. It works by packaging the web app in a `.webpkg` file, a special kind of zip file designed for distributing web apps. 
## Use Cases
* In third-world countries, web apps and games can be distributed P2P and run in any client that reads these packages
## WebPackage vs. PWA
* put something here
## Structure
The structure of a `.webpkg` contains a folder with named the id of the app with .app at the end snd contains two folders, a `app` folder and a `meta` folder. The `app` folder is where you store all of the code, such as html, css, and javascript files. The `meta` folder is where you store an icon and a `package.json` file. `local-package.json` is where the client stores user specific information that would not make sense to be distributed. 
general layout:  
name.webpkg  
|- name.app/  
|-- meta/  
|--- package.json  
|--- local-package.json  
|--- icon.png  
|-- app/  
|--- index.html  
|--- ...  

### package.json
a general layout of the `package.json`:
```
{
  "id": "foo",
  "title": "bar",
  "author": "John Doe",
  "version": "1.0",
  "icon": "icon.png"
}
```
