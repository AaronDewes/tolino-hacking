# Reading and writing the reseller config

---

These modifications require your Tolino to be connected to the internet.

---

Modifying the reseller config makes it possible to change the browser start page for example.


## Reading the configuration

To get the reseller configuration, simply connect your Tolino to a computer via USB and create an empty file called `reseller.dump` (On Windows, be careful so it's not reseller.dump.txt).
Then disconnect the Tolino, reboot it and wait 5 minutes.

After waiting, if you connect your Tolino via USB again, it should show the reseller config in the `reseller.dump`.


## Modifying the configuration

This requires an exisiting reseller configuration in a `reseller.dump`.

1.  Rename the `reseller.dump` to `reseller.conf`.
2.  Open the file in a text editor.
3.  Change values, but be careful to keep the file in valid JSON. Please note that overwriting some of the values in this file can lead to breaking the online features.

As a suggested change, if you want to go back to Google for searching, change

The `URL_BROWSER_SEARCH_PAGE` like this: `"URL_BROWSER_SEARCH_PAGE":"https://google.de/search?q=%s"`

You can also change the browser start page `URL_BROWSER_START_PAGE`: `"URL_BROWSER_START_PAGE":"https://google.de/"`


### Going back to the original configuration

To revert these changes, just delete the `reseller.conf` and reboot your Tolino.
