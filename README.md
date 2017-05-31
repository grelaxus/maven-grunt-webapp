# maven-grunt-webapp
The original discussion is [here](https://stackoverflow.com/questions/25855873/java-gulp-and-maven-folder-structure).
This is an option A

I'm currently using Java + Grunt + Maven. I've found there are two ways of packaging your frontend with your backend and the same will certainly apply to Gulp.

In the end it's up to what's best for your project/team. From my experience I usually use option B when working with others since the decoupling is easily worth the other issues. When I'm doing my own side projects I always go for option A because it's just easier to launch one webserver and to run a local environment closer to what DEV/PROD is like.

A) Put your frontend into the webapp folder (ex. https://github.com/kdubb1337/maven-grunt-webapp)

Benefits - You can launch your backend and do development all in one place and working with Spring security is a snap, even without OAUTH. Fewer issues working with two webservers up on your local environment when they would normally be bundled into one port on other environments.

B) Keep your frontend in a different folder, or even in a different repo that you clone into the root folder of your backend repo. (ex. https://github.com/kdubb1337/maven-grunt) see the 'yo' folder

Benefits - Fantastic decoupling so front end developers can live in joy without having to even install java locally or worry about recompiling your backend. Works great if you want Travis (or your favourite CI app) to do unit tests on the backend and the frontend.

EDIT I've found this awesome plugin you can use with maven/gradle to build the frontend https://github.com/eirslett/frontend-maven-plugin. Seems like the way to go, will be refactoring my starter projects with this guy for grunt and gulp
