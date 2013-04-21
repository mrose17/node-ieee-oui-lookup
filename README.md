node-ieee-oui-lookup
====================

A node.js module to fetch, parse, and lookup entries from the IEEE's OUI database.

Install
-------

    npm install ieee-oui-lookup

Usage
-----

    var oui = require('ieee-oui-lookup');

When loaded, the module will, if needed, fetch the IEEE OUI registry and make a database.

To lookup a MAC prefix:

    oui.lookup('AB-CD-EF', function(err, name) { ... });

If _err_ is an object, then _name_ is irrelevant; otherwise, _name_ is either a _string_ (hit) or _null_ (miss).

Example
-------

    oui.lookup('FF-FB-FB', function(err, name) {
      if (err) console.log('FF-FB-FB: ' + err.message); else console.log('FF-FB-FB -> ' + name);
    });

License
-------

MIT. Freely have you received, freely give.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

