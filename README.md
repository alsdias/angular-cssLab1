## BOOTSTRAP MANUAL INSTALL - METHOD 1



![img](https://ultering.com/it4us/wp-content/uploads/2021/01/angular_cssLab1-1.jpg)

**1. Download:**

\- latest version:
[getbootstrap.com/](https://getbootstrap.com/)

\- prior versions:
[v.3.3](https://getbootstrap.com/docs/3.3/getting-started/#template)
[v.3.3.7](http://blog.getbootstrap.com/2016/07/25/bootstrap-3-3-7-released/)
[v.4.5](https://getbootstrap.com/docs/4.5/getting-started/download/)

**2. Extract to style dir:**

mkdir styles
xcopy ...\bootstrap-4.5.3-dist ..\PROJECT_ROOT\src\styles /Y/S/I/E



![img](https://ultering.com/itstuff/wp-content/uploads/2021/01/angular_manual_bootstrap_install_cssLab1.jpg)



**3. Import the CSS.**

Two alternatives:

**3a. Edit "angular.json" and set:**

	"styles": [
		"src/styles.css",
		"src/styles/bootstrap-4.5.3-dist/css/bootstrap.css",
		"src/styles/css/album.css"
	],
or

**3b. Use import:**
@import './styles/bootstrap-5.0.0-beta1-dist/css/bootstrap.min.css';



**4. If desired jquery, do:**
npm install jquery popper.js –save

   Edit angular.json and set:

            "scripts": [
            	"node_modules/jquery/dist/jquery.js",
            	"node_modules/popper.js/dist/umd/popper.js",
            	"node_modules/bootstrap/dist/js/bootstrap.js"
            ]


***\**IMPORTANT NOTE:**
Don't use the assets directory to set the CSS files.
When deploying to the production using Angular CLI, the CSS files registered in angular.json are minified and bundled into a single styles.css.
The assets folder is copied to the dist folder during the build process then, the CSS code get duplicated.
Only place CSS files under assets if importing them directly in the index.html.

 
