## The Nmap Scripting Engine
* Located in /usr/share/nmap/scripts
* Scripts fall into serveral categories:
  * info gathering
  * active vulnerability assessment
  * searches for signs of previous compromises and much more.
* To get info about a category of scripts or a specific one...
  * nmap --script-help default
  * This will display info regarding the default scripts
* Running **nmap -sC someIP** will run all the scripts in the default category

## Exploring a Strange Port
* If you try scanning port 3232 with an nmap version scan it will crash.
* this behavior suggests that the listening program is designed to listen for a particular input and that it
has difficulty processing anything else.
* By going to the url bar and visiting someIP:3232 we see that it's a web page. Not much may be displayed.
* Connect to the port via netcat.
 * **nc someIp 3232**
 * Ask the web server for the default page: **GET / HTTP/1.1**
 * Server will respond with it's name and version.
 
 ## Finding Valid Usernames
 * Increase chances of successful password attack by finding valid usernames for services via the VRFY SMTP command.
 * **nc someIP 25**
 * **VRFY username**
