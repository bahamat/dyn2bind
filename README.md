# dyn2bind

A short program utilizing the [Dyn](http://www.dynect.com) API to make a copy of all of your DNS zones in Dyn and save them in Bind compatible zone file format.

I wrote this since Dyn supports [axfr in][axfr-in] but not [out][axfr-out].

[axfr-in]: https://help.dyn.com/primary-zone-transfer-api/
[axfr-out]: http://www.dyncommunity.com/questions/7647/how-do-i-enable-axfr.html

## Bugs

Not all record types supported by the Dyn API are supported by dyn2bind. If you encounter one, send me the JSON output and I can add support, or feel free to open a pull request.

Some record types supported by the Dyn API are considered experimental by dyn2bind. This is because I don't happen to use them but implementation looked pretty simple. You should verify these records before using any resulting zone files.

There is no support for services other than DNS (e.g., HTTP redirect, load balancing, etc.).
