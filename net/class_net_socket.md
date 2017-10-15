<!-- YAML
added: v0.3.4
-->

This class is an abstraction of a TCP socket or a streaming [IPC][] endpoint
(uses named pipes on Windows, and UNIX domain sockets otherwise). A
`net.Socket` is also a [duplex stream][], so it can be both readable and
writable, and it is also a [`EventEmitter`][].

A `net.Socket` can be created by the user and used directly to interact with
a server. For example, it is returned by [`net.createConnection()`][],
so the user can use it to talk to the server.

It can also be created by Node.js and passed to the user when a connection
is received. For example, it is passed to the listeners of a
[`'connection'`][] event emitted on a [`net.Server`][], so the user can use
it to interact with the client.

这个类是一个 TCP socket 或者一个流动的 [IPC][] 端点的抽象（在Windows上使用命名管道，而UNIX使用域套接字）。一个`net.Socket`也是一个[duplex stream][]，所以它能被读或写，并且它也是一个[`EventEmitter`][]。

一个`net.Socket`能被用户创建并且直接使用，来与一个server通信。举个例子，它是通过[`net.createConnection()`][]返回的，所以用户可以使用它来与server通信。

当一个连接被接收时，它也能被Node.js创建并传递给用户。比如，它是通过监听在一个[`net.Server`][]上的[`'connection'`][]事件触发而获得的，那么用户可以使用它来与客户端通信。
