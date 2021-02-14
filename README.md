# Rmd160-js
This repository contains a RIPEMD-160 hashing algorithm provided as a single
javascript function that can easily be integrated into browser based
applications.

The motivation for writing this piece of code came from the dire need to have a
simple, easy-to-use javascript implementation of the RIPEMD-160 algorithm that
would just work in a web browser. The existing implementations were no good
because they were either delivered via the TypeScript/NodeJs anti-patterns or
used some repulsive license such as The BSD License.

[Ripemd160-min](https://github.com/zone117x/ripemd160-minimal.js) was used as a
basis of this work due to the fact that it was released under the MIT license.

# Progressive hashing
```js
var hasher = rmd160();
hasher = rmd160(new Uint8Array(str2utf8_array("x")), hasher);
hasher = rmd160(new Uint8Array(str2utf8_array("x")), hasher);
hasher = rmd160(new Uint8Array(str2utf8_array("x")), hasher);
console.log(rmd160(null, hasher));
```

# Quick hashing
```js
console.log(rmd160(new Uint8Array(str2utf8_array("xxx")));
```
