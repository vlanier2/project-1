# UOCIS322 - Project 1 #

NAME: Vincent Lanier

CONTACT: vlanier@uoregon.edu

# Project description

This project implements a simple webserver using the
python socket package. For now, the server responds
only to GET requests.

## Setup

credentials-skel.ini should be replaced by a credentials.ini
file specifying the port, folder path, and logging level.
If no credentials file is provided, it defaults to port 5000
and ./pages.

Start the server with 
```
make start
```

## Usage

The server will serve files contained in DOCROOT. The server
will respond with "401 not implemented" to any requests other 
than GET. "403 Forbidden" is sent for disallowed characters
and "404 not found" is sent if the requested file is not located
in DOCROOT.

A sample docroot is provided (./pages).

### Example
```
Request:
curl -X GET "localhost:5000/trivia.css"

Response:
/*
 * Trivial style sheet for a trivial page
 */

body { background-color: rgb(200,255,200); }
p { color:  rgb(200,0,0); }
```

## Shutting Down

Shut down the server with
```
make stop
```
The stop script should shut down the server process. the process
ID is printed in case the process continues running and must
be manually killed.