# Using bitcore-lib with Peercoin

This repository shows how to use [bitcore-lib](https://github.com/bitpay/bitcore/tree/master/packages/bitcore-lib) for Peercoin development in javascript.  

[patch-package](https://www.npmjs.com/package/patch-package) is being used to patch the upstream bitcore-lib and allow it to handle Peercoin specifics.  
In order to use `patch-package` you must drop the `patches` directory into you work directory and edit the `package.json` to include `"postinstall": "patch-package"` in the `"scripts"` section.  
See the attached `package.json` file for the example.

Using patch-package simplifies the process of adapting upstream bitcore-lib to work with Peercoin as all developers must worry about is the local bitcore-lib.*.patch.

Upon running "npm install" you will notice message like in the log:
```
"Applying patches...
bitcore-lib@8.25.25 ✔
```

Which means that bitcore-lib has been patched upon installation.
Sweet.


## Older version

This older patch may be useful if you are handling older, v=1 transactions.

https://github.com/peercoin/bitcore-ppc/blob/master/bitcore-ppc.js