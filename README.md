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

If _err_ is an object, then _name_ is irrelevant; otherwise _name_ is either a _string_ (hit) or _null_ (miss).

Example
-------

    oui.lookup('FF-FB-FB', function(err, name) {
      if (err) console.log('FF-FB-FB: ' + err.message); else console.log('FF-FB-FB -> ' + name);
    });

License
-------

MIT. Freely have you received, freely give.
node-ieee-oui-lookup\n====================\n\nA node.js module to fetch, parse, and lookup entries from the IEEE's OUI database.\n\nInstall\n-------\n\n    npm install ieee-oui-lookup\n\nUsage\n-----\n\n    var oui = require('ieee-oui-lookup');\n\nWhen loaded, the module will, if needed, fetch the IEEE OUI registry and make a database.\n\nTo lookup a MAC prefix:\n\n    oui.lookup('AB-CD-EF', function(err, name) { ... });\n\nIf _err_ is an object, then _name_ is irrelevant; otherwise _name_ is either a _string_ (hit) or _null_ (miss).\n\nExample\n-------\n\n    oui.lookup('FF-FB-FB', function(err, name) {\n      if (err) console.log('FF-FB-FB: ' + err.message); else console.log('FF-FB-FB -> ' + name);\n    });\n\nLicense\n-------\n\nMIT. Freely have you received, freely give.\n