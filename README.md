# openhab-mcedit
## Description
syntax files for mcedit

## Installing
* copy the syntax-files to /usr/share/mc/syntax/
* copy'n'paste the following lines to the file "Syntax"

```
file ..\*\\.(items)$ openHAB\sItems 
include openhab-items.syntax  
 
file ..\*\\.(sitemap)$ openHAB\sSitemap 
include openhab-sitemap.syntax
 
file ..\*\\.(persist)$ openHAB\sPersistence
include openhab-persist.syntax
 
file ..\*\\.(rules)$ openHAB\sRules
include openhab-rules.syntax 
```

* edit the Debian-line from `file (rules|rocks)$ Debian\srules` to `file (rocks)$ Debian\srules`, because it interferes with openhabs rules-files 