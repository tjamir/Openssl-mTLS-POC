# Openssl mTLS POC
A client-server example using mTLS through Openssl

## Compiling

In order to compile the server and the client, you'll need `libssl` and `libcrypto` installed in your system.

### Compiling the Server


```
cd src
gcc -Wall -o server server.c -L/usr/lib -lssl -lcrypto
```

### Compiling the client

```
cd src
gcc -Wall -o client client.c -L/usr/lib -lssl -lcrypto 
```

## Running

### Running the Server

```
cd src
./server
```

### Running the Client

Before running the client, you must choose one of the certificate pair files. `client1.*` files are signed with the CA1 keys, which are the same as the server certificate. `client2.*` files are signed with CA2 files. So, if you are running with `client2` files, a error should be expected.
