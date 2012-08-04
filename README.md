A simple, tiny, nicely embeddable HTTP 1.0 (partially 1.1) server in Java
Adapted for Android!

NanoHTTPD version 1.25 (android edition),
Copyright (c) 2001,2005-2012 Jarno Elonen (elonen@iki.fi, http://iki.fi/elonen/)
Copyright (c) 2010 Konstantinos Togias (info@ktogias.gr, http://ktogias.gr)
Copyright (c) 2012 Andrew Brampton (http://bramp.net)

Features & limitations
======================

* Only one Java file
* Released as open source, Modified BSD licence
* No fixed config files, logging, authorization etc. (Implement by yourself if you need them.)
* Supports parameter parsing of GET and POST methods (+ rudimentary PUT support in 1.25)
* Supports both dynamic content and file serving
* Supports file upload (since version 1.2, 2010)
* Supports partial content (streaming)
* Supports ETags
* Never caches anything
* Doesn't limit bandwidth, request time or simultaneous connections
* Default code serves files and shows all HTTP parameters and headers
* File server supports directory listing, index.html and index.htm
* File server supports partial content (streaming)
* File server supports ETags
* File server does the 301 redirection trick for directories without '/'
* File server supports simple skipping for files (continue download)
* File server serves also very long files without memory overhead
* Contains a built-in list of most common mime types
* All header names are converted lowercase so they don't vary between browsers/clients

Ways to use
===========

* Run as a standalone app, serves files and shows requests
* Subclass serve() and embed to your own program (see HelloServer.java for a simple example)
* Call serveFile() from serve() with your own base directory
