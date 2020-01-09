Container for accessing IPMI/OOB consoles, designed to work with as many servers as possible.

# Running
`docker run --rm -it -p 8080:8080 fresta/ipmi-console`  
Go to http://127.0.0.1:8080/vnc.html in your browser and press "Connect".  
Use firefox in the container and connect to your IPMI console.

# In container

* xvfb - virtual x11 display server
* x11vnc - view and interact with x displays remotely
* [noNVC](https://kanaka.github.io/noVNC/) - A HTML5 canvas vnc viewer
* novnc - vnc web client
* Fluxbox - windowmanager
* Firefox - browser
* java - needed to access most ipmi consoles

