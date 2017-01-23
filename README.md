# openhab-mcedit
## Description
syntax files for mcedit

## Installing

To install the syntax highlighting execute these commands

```
# download insert new triggers to Syntax file
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

```
