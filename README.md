[jQuery](http://jquery.com/) [Ajax](http://api.jquery.com/category/ajax/) + [Deferreds](http://api.jquery.com/category/deferred-object/)
==================================================

JQuery is great, but its greatness comes at a cost. Sometimes you wish you could extract just a few of its modules and though [it's possible](https://github.com/jquery/jquery#how-to-build-your-own-jquery) it can still end up being quite heavy.

jQuery Ajax + Deferreds (jQXD) is a fork of jQuery v2.1.0 that leaves jQuery core with only two of its most popular modules (Ajax & Deferred) and strips out the rest. The result is an AJAX library with a lighter footprint (14 KB -minified) and an awesome (and well-known) API that can be used in browser and non-browser environments.

How to build this project
----------------------------

Clone a copy of the repo by running:

```bash
git clone https://github.com/quiaro/jquery-ajax.git
```

Enter the project's directory and run the build script:
```bash
cd jquery-ajax && npm run build
```

The built version of the project will be put in the `dist/` subdirectory, along with the minified copy and associated map file.

Also, by running the `grunt` command, in the `jquery-ajax` directory, you are able to build the project (just like with `npm run build` command):
```
grunt
```

To look at the other tasks available inherited from the jQuery project, try the -help option for grunt:
```
grunt -help
```

Building to a different directory
---------------------------------

To copy the built jQuery files from `/dist` to another directory:

```bash
grunt && grunt dist:/path/to/special/location/
```
With this example, the output files would be:

```bash
/path/to/special/location/jquery-ajax.js
/path/to/special/location/jquery-ajax.min.js
```

To add a permanent copy destination, create a file in `dist/` called ".destination.json". Inside the file, paste and customize the following:

```json

{
  "/Absolute/path/to/other/destination": true
}
```

Additionally, both methods can be combined.



