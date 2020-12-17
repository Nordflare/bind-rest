_**Notice**: This project is currently in development and is prone to issues, do not use it in a production environment (yet) and if you come across any issues while testing it for yourselves please report them in the issues tab._

# BIND DNS RESTful API

bind-rest is a RESTful API implementation for the BIND DNS server written in Node.js with help from EJS to manage files. 

## What is it?

## How does it work?

The API uses JSON to communicate with end users and stores its data in JSON via a database (currently undecided). When the zone JSON is modified it is parsed into BIND zone file format and the zone file is updated. The reason for this is for ease of adding DNS records or modifying the zone. The reason this is beneficial is because changing and replacing data in the zone files themselves is a fairly dangerous task and could easily break a file if the code is even slightly off, however, using JSON eliminates this problem because instead of replacing zone files we re-create them by parsing data from the JSON zone object. And because the zones are primarly stored in JSON format we can easily add, remove and modify all parts of the zone thanks to the fact that it is all key:value based.
