## Check to see if updates has been made to export_rfc8416_dn42.json every 3rd hour.

```
54 */3 * * * file="$HOME/export_rfc8416_dn42.json" ; uri="https://git.dn42.us/netravnen/dn42-roa-export/raw/master/export_rfc8416_dn42.json" ; if test -e "$file" ; then zflag="-z " ; else zflag= ; fi ; curl -s -o "$file" $zflag "$uri"
```
