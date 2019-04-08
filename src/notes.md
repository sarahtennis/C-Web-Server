##### Files
- net.h and net.c
  - contain low-level networking code
- mime.h and mime.c
  - contains functionality for determining the MIME type of a file
- file.h and file.c
  - contains handy file-reading code that you may want to utilize, namely the file_load() and file_free() functions for reading file data and deallocating file data, respectively (or you could just perform these operations manually as well)
- hashtable.h and hashtable.c
  - contain an implementation of a hashtable (this one is a bit more complicated than what you built in the Hashtables sprint)
- llist.h and llist.c
  - contain an implementation of a doubly-linked list (used solely by the hashable--you don't need it)
- cache.h and cache.c
  - are where you will implement the LRU cache functionality for days 3 and 4

##### Day 1/Day 2
- Implement send_response()
  - format HTTP response
  - write response to ```response``` variable
  - ```response_length```: total length of header and body (how many bytes to send)
  - ```content_length```: length of body only
- handle_http_request() in the file server.c
  - direct to correct response
- Implement arbitrary file serving
  - map to serverroot directory to check for files
  - use functionality in file.c
  - use mime.c for Content-Type header information

##### Run Server
- make
- ./server

