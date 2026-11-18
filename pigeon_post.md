# Pigeon post module development

## Location of config.json file
The distinction between config.json in the pigeon_post repo and config.json in the working directory is one that tripped me up too!
I've omitted an essential configuration step from the README:
A client program importing pigeon_post/config should copy the file into it's local directory. 

This reflects the fact that the client now owns this particular configuration, and is responsible for making it coincide with a particular instance of a server, that also happens to support the pigeon_post communication standard.
