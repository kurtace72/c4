# c4
:fire: a javascript engine burster error handler

Burst [nodejs] or a [browser] engine in case an hacking error was detected.

## Installation

```bash
npm i --save c4
```

## Usage

In case you catch an error

```js
var C4 = require( 'c4' )

var bomb = new C4({
    delay: 20 // ms
})

function someMethod ( variable ) {
    try{
        if ( variable === 'hacking' ) {
            throw new Error( "Hacking errorr!!!!!" )
        }
    }catch(err) {
        report(function () {
            document.body.innerHtml = "i know what you did boy... reported!!"
            bomb.explode()
        })
    }
}

```

## Options

```js
{
    wipeGlobal: true,
    wipeDocument: true,
    wipeRequire: true,
    delay: 300,
}
```
