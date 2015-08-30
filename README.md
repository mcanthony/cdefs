# node-cproto

Extract function prototypes from C source files.

### Install

```bash
$ npm install cproto -g
```

### Usage

#### from command-line

Inspect ```example.c``` and print prototypes to ```stdout```.

```bash
$ proto example.c
{ main: { returns: 'int', arguments: [ 'int argc', 'char** argv' ] },
  test: { returns: 'float', arguments: [] },
  print: { returns: 'void', arguments: [ 'char * str' ] } }
```

Inspect ```example.c``` and save prototypes to ```example.json```:

```bash
$ proto example.c -o example.json
```

#### from your module

```javascript
var proto = require('cproto');
console.log(proto('example.c'));  
```

### Contribute

Contributions are welcome.
