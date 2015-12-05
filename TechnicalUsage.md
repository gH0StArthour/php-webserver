# Install #
  1. Download the latest version from the downloads and unzip it.
  1. Move `WebServer.php` to your application's directory.

# Usage #
  1. Include `WebServer.php` in your application.
```
require_once "WebServer.php";
```
  1. Initialise the object.
```
$ws = new WebServer();
```
  1. Handle the requests by passing a callback function by name, or a class and method, or an instance and method.
```
$ws->handleRequests("myFunction");
// or
$ws->handleRequests("MyClass", "myMethod");
// or
$ws->handleRequests($my_instance, "myMethod");
```
  1. Write the callback function/method.
```
function myFunction($webserver) {
 var_dump($_SERVER);
}
```

# Run #
  1. Open a Terminal and navigate to your application.
```
$ login
$ cd ~/MyApps/MyWebApp/
```
  1. Run the application. _Note: `sudo` must be used if the port is below 1024._
```
$ php myphpscript.php
// [or]
$ sudo php myphpscript.php
```
  1. The server will continue to run until you quit it (^C - Control + C).