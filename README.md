# angular-cssLab1


## BOOTSTRAP MANUAL INSTALLATION

(2.1: Alternative: Local Bootstrap CSS)
As an alternative, you can also download the Bootstrap CSS and add it locally to your project. 
I donwloaded Bootstrap from the website and created a folder styles (same level as styles.css):
@@img;;M:\work\devcli_\javascript\jstopics_bitbucket\cssLab1\support\docs\nodejs_local_bootstrap_install.jpg

1. Download:
https://getbootstrap.com/

2. Extract to style dir:
mkdir styles
xcopy ...\bootstrap-4.5.3-dist  ..\PROJECT_ROOT\src\styles /Y/S/I/E


3. Import the CSS.
Two alternatives:

3a. Edit "angular.json" and set:

	"styles": [
	  "src/styles.css",
	  "src/styles/bootstrap-4.5.3-dist/css/bootstrap.css",
	  "src/styles/css/album.css"
	],

or

3b. Use import:  
  @import './styles/bootstrap-5.0.0-beta1-dist/css/bootstrap.min.css';

4. If desired jquery, do:
    npm install jquery popper.js –save

***IMPORTANT NOTE:
Don't use the assets directory to set the CSS files.
When deploying to the production using Angular CLI, the CSS files registered in angular.json are minified and bundled into a single styles.css. 
The assets folder is copied to the dist folder during the build process then, the CSS code get duplicated. 
Only place CSS files under assets if importing them directly in the index.html. 


