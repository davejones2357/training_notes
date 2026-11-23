# Implementing a CLI for HQ & green_corsair.

As it stands, client and server have a single execution path.

When the server is runs, it reads the accepted clients data file and awaits a connection from one of them, displaying a 'valid connection' message when one arrives. 
When the client is run, it sends a connection message with a hard coded client ID, then terminates.

The next step is to provide a CLI for both programs, initially with just a start command which wraps current functionality. 

After that, the client can have a --client <clientID> option which improves on the hard coded clientID.
