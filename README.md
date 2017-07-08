# openhab-mcedit
## Description
syntax files for mcedit

## Installing

To install the syntax highlighting execute these commands

```bash
# download syntax files for openhab files
sudo curl -L -o /usr/share/mc/syntax/openhab-items.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-items.syntax
sudo curl -L -o /usr/share/mc/syntax/openhab-persist.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-persist.syntax
sudo curl -L -o /usr/share/mc/syntax/openhab-rules.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-rules.syntax
sudo curl -L -o /usr/share/mc/syntax/openhab-sitemap.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-sitemap.syntax
sudo curl -L -o /usr/share/mc/syntax/openhab-script.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-script.syntax

# download and apply patch for Syntax file
curl -L -o /tmp/Syntax.patch https://github.com/CWempe/openhab-mcedit/raw/master/Syntax.patch
sudo patch /usr/share/mc/syntax/Syntax < /tmp/Syntax.patch
```
