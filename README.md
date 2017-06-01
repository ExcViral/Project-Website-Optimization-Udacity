## Website Performance Optimization portfolio project

This Project is a part of the [Udacity Front-End Web Developer Nanodegree](https://www.udacity.com/course/front-end-web-developer-nanodegree--nd001) programme.


The original github repository for this project can be found [here](https://github.com/udacity/frontend-nanodegree-mobile-portfolio)

The objective of this project was to optimize a provided website so that it achieves a target PageSpeed score of atleast 90 and renders at around 60 frames per second, so that user has a jank free experience.

The project folder contains two main folders:
* **dist /** _contains the production code_
* **src /** _contains the source code_

Gulp has been used in this project for optimizing the source code. If you are unfamiliar to Gulp, I recommend going through [this guide of CSSTricks](https://css-tricks.com/gulp-for-beginners/).

### Getting started
### How to run the website ?
##### Run locally using python server
 1. Clone or Download this repository to your computer:
 ```
 # Run the following commands in Terminal :
 $ git clone https://github.com/ExcViral/Project-Website-Optimization-Udacity.git
 ```
 2. Navigate to the dist/ directory inside the the project folder and start the python webserver:
 ```
 # Run the following commands in Terminal :

 $ cd Project-Website-Optimization-Udacity
 $ cd dist

 # I am using port 8000 to run the server. To change port number substitute 8000 in the command below with your desired port number.
 # now start the python webserver using the following command :

 $ python -m http.server 8000
 ```
 3. Now open browser and type the following address in the address bar :
 ```
 127.0.0.1:8000
 ```

##### Tunneling your website using Ngrok
 1. Download Ngrok from the [official website](https://ngrok.com/). Save it inside the project folder.
 2. Unzip it inside the folder dist /
 ```
  # Open Terminal inside the dist folder and run the following command :
  $ unzip ../ngrok*
 ```
 3. Now start a local python server using the instructions given above.
 4. Now start Ngrok tunnel :
 ```
 # Open Terminal inside the dist folder and run the following command :
$ ./ngrok http 8000
 ```
 5. Now the Ngrok tunnel must have started. Your Terminal will display information about the tunnel. You will find a link in the _Forwarding_ label, copy and paste that link in your browser. If you have done everything correctly, you will see the website load in the browser window.

### How to make changes to website ?
As mentioned above, the source code is located inside the _src /_ folder and the production code (minified and opimized) is located inside _dist /_ folder.<br>
Make the changes you want to the files inside the _src /_ folder.<br>
 To automatically generate production code, you will need to set up Gulp. Follow the instructions below :

##### Setting up Gulp
  1. Make sure you have _Node Js_ installed on your system. If not, you can find the installation guide [here](https://nodejs.org/en/download/package-manager/).
  2. Install Gulp (_Skip this step if you have gulp installed on your system_)
  ```
  # Run the command below in your Terminal :
  $ sudo npm install gulp -g
  ```
  3. Navigate to the root of project folder and follow these instructions :
  ```
  # Open Terminal inside the root of project folder and run the following commands :

  $ npm i
  $ npm install --save-dev gulp-uglify gulp-minify-css gulp-htmlmin gulp-image-optimization gulp-webserver

  # Type the following command to check if Gulp has been set up properly :

  $ gulp

  # If you have followed the steps correctly, You should now see gulp starting and running specified tasks in the gulpfile.js
  ```
  4. Now you have finished setting up Gulp inside the project folder. Whenever you make changes, and you want to generate production code, just open Terminal inside root of project folder and run `$ gulp `, The production code will be automatically generated and saved inside dist folder.


#### Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
