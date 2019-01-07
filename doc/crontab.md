## Update ROA file

Check to see if updates has been made to export_rfc8416_dn42.json every 6th hour.

```
54 */6 * * * file="$HOME/export_rfc8416_dn42.json" ; uri="https://git.dn42.us/netravnen/dn42-roa-export/raw/master/export_rfc8416_dn42.json" ; if test -e "$file" ; then zflag="-z " ; else zflag= ; fi ; curl -s -o "$file" $zflag "$uri"
```
