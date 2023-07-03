# PlexRakNet

This is the Raknet library that used for the Plex server software, it is originally made by GoMint.

## Usage

Supports both server-side and client-side connections through two different types of sockets.

Creating a client socket:
```Java
ClientSocket client = new ClientSocket();
client.setEventHandler( handler );
try {
    client.initialize()
} catch ( SocketException e ) {
    logger.error( "Failed to initialize client socket", e );
}
client.connect( "127.0.0.1", 19112 );
```

Creating a server socket:
```Java
ServerSocket server = new ServerSocket( 10 );
server.setEventHandler( handler );
try {
    server.bind( "0.0.0.0", 19112 );
} catch ( SocketException e ) {
    logger.error( "Failed to bind server socket", e );
}
```

## Authors

PlexRakNet was originally developed by BlackyPaw with the support of geNAZt for several tests for GoMint.

