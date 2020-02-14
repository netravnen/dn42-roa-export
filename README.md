## Notes

- These files are Bird 1.x compatible:
  - [bird_roa_dn42.conf](bird_roa_dn42.conf)
  - [bird4_roa_dn42.conf](bird4_roa_dn42.conf)
  - [bird6_roa_dn42.conf](bird6_roa_dn42.conf)
- These files are Bird 2.x compatible:
  - [bird_route_dn42.conf](bird_route_dn42.conf)
  - [bird4_route_dn42.conf](bird4_route_dn42.conf)
  - [bird6_route_dn42.conf](bird6_route_dn42.conf)
- These files are [Routinator][2] compatible:
  - [export_rfc8416_dn42.json](export_rfc8416_dn42.json) _(SLURM standard, format specified in [RFC 8416][4])_
- These files are [gortr][3] compatible:
  - [export_dn42.json](export_dn42.json)

Note the gortr file is DateTime stamped only, it is not signed with any certificaty. So you will need to add
`-verify=false` as a runtime parameter when loading the cache file.

## [Last merge commit][0] at [dn42 registry][1]

```
commit 1c3bae223ba85fb3117b44e802f705fdbf365dfc
Merge: 570600d6 2ace2efb
Author: burble
Date:   2020-02-14 14:22:35 +0000

    Merge branch 'master' of XYenon/registry into master
```

## crontab

You can setup a [cronjob][5] to check in with updates to the ROA files listed
above on regular intervals.

Currently the ROA files published here is refreshed every 6th hour if
updates has been made to the [DN42 registry][1].

## Misc statistics

- ROAs IPv4:  1109
- ROAs IPv6:  849
- ROAs total: 1958

[0]: https://git.dn42.us/dn42/registry/commit/1c3bae223ba85fb3117b44e802f705fdbf365dfc
[1]: https://git.dn42.us/dn42/registry
[2]: https://github.com/NLnetLabs/routinator
[3]: https://github.com/cloudflare/gortr
[4]: https://tools.ietf.org/html/rfc8416
[5]: doc/crontab.md

