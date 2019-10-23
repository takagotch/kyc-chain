### kyc-chain
---
https://kyc-chain.com/

https://github.com/rudrakhp/KYC-chain

```js
// root/node_modules/hash-base
const HashBase = require('hash-base')
const inherits = require('inherits')

function MyHash () {
  HashBase.call(this, 1)
  
  this._sum = 0x00
}

inherits(MyHash, HashBase)

MyHash.prototype._update = function () {
  for (let i = 0; i < this._block.length; ++i) this._sum ^= this._block[i]
}

MyHash.prototype._digest = function () {
  return this._sum
}

const data = Buffer.from([ 0x00, 0x42, 0x01 ])
const hash = new MyHash().update(data).digest()
console.log(hash)
```

```
```

```
```

