# openhab-mcedit
## Description
syntax files for mcedit

## Installing

To install the syntax highlighting execute these commands

```bash
# download and insert new triggers to Syntax file
sudo curl -L -o /tmp/Syntax_insert https://github.com/CWempe/openhab-mcedit/raw/master/Syntax_insert
sudo mv /usr/share/mc/syntax/Syntax /usr/share/mc/syntax/Syntax.backup

# add all previous shemes exept 'unknown'
head -n -2 /usr/share/mc/syntax/Syntax.backup | sudo tee /usr/share/mc/syntax/Syntax

# remove debian .rules  to make openhab .rules work
sudo sed -i s/rules\|rocks/rocks/ /usr/share/mc/syntax/Syntax

# insert openhab parts
cat /tmp/Syntax_insert | sudo tee -a /usr/share/mc/syntax/Syntax

# add 'unknown' part
tail -n -2 /usr/share/mc/syntax/Syntax.backup | sudo tee -a /usr/share/mc/syntax/Syntax

sudo rm /tmp/Syntax_insert


# download syntax files for openhab files
sudo curl -L -o /usr/share/mc/syntax/openhab-items.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-items.syntax
sudo curl -L -o /usr/share/mc/syntax/openhab-persist.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-persist.syntax
sudo curl -L -o /usr/share/mc/syntax/openhab-rules.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-rules.syntax
sudo curl -L -o /usr/share/mc/syntax/openhab-sitemap.syntax https://github.com/CWempe/openhab-mcedit/raw/master/openhab-sitemap.syntax

```
