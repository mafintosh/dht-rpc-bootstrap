# dht-rpc-bootstrap

Easily spin up a [dht-rpc](https://github.com/mafintosh/dht-rpc) bootstrap node from the command line.

```
npm install dht-rpc-bootstrap
```

## Usage

A bootstrap node is just a normal dht node, except it doesn't answer any custom queries and will
just forward you to other nodes in the network.

``` sh
dht-rpc-bootstrap --port=10000
```

After spinning up a node add it to your dht-rpc bootstrap list

``` js
var node = dht({
  bootstrap: ['mydomain.com:10000']
})

var stream = node.query({
  command: 'cool-stuff',
  target: ...
})
```

## License

MIT
