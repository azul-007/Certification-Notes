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
