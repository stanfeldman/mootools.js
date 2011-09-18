# MooTools 1.4.0 Server

For more information about mootools visit http://mootools.net
MooTools is a compact, modular, Object-Oriented JavaScript framework designed for the intermediate to advanced JavaScript developer.
It allows you to write powerful, flexible, and cross-browser code with its elegant, well documented, and coherent API.

Mootools Server is a customized MooTools build without any component relative to browsers. Includes Class, Core and Native Extensions.
Christoph Pojer have added wrapper and loader for node.js.

# Installation

* Get npm (http://npmjs.org)
* run <pre>npm install mootools</pre>
* Done

# Usage
<pre>
require("./mootools").apply(GLOBAL);

var Controller = new Class
({
	get: function(req, res) { not_found(); },
	
	post: function(req, res) { not_found(); },
	
	put: function(req, res) { not_found(); },
	
	del: function(req, res) { not_found(); },
	
	not_found: function()
	{
		res.writeHead(200, {'Content-Type': 'text/html'});
		res.end("404");
	}
});

var Controller1 = new Class
({
	Extends: controllers.Controller,
	
	get: function(req, res)
	{
		var result = "hello world!";
		res.writeHead(200, {'Content-Type': 'text/html'});
		res.end(result);
	}
});
</pre>
