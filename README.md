## Notes

- These files are Bird 1.x compatible:
  - [bird_roa_dn42.conf](bird_roa_dn42.conf)
  - [bird4_roa_dn42.conf](bird4_roa_dn42.conf)
  - [bird6_roa_dn42.conf](bird6_roa_dn42.conf)
- These files are Bird 2.x compatible:
  - [bird_route_dn42.conf](bird_route_dn42.conf)
  - [bird4_route_dn42.conf](bird4_route_dn42.conf)
  - [bird6_route_dn42.conf](bird6_route_dn42.conf)
- These files are [Routinator][2] and [gortr][3] ([src][6]) compatible:
  - [export_rfc8416_dn42.json](export_rfc8416_dn42.json) _(SLURM standard, format specified in [RFC 8416][4])_
- These files are [gortr][3] compatible:
  - [export_dn42.json](export_dn42.json)

Note the gortr source file is DateTime stamped only, it is not signed with any certificaty. So you will need to add
`-verify=false` as a runtime parameter when loading the cache file. Alternatively, use gortr with a slurm file
instead (e.g. ) as a command-line parameter.

## [Last merge commit][0] at [dn42 registry][1]

```
commit 3a7ca794813b3dbdd3c435d95875a7d9c60bd30b
Merge: d0beb3d3 a63ac1c6
Author: Simon Marsh <burble@noreply.dn42.us>
Date:   2020-07-18 18:14:34 +0000

    Merge pull request 'Updated AS4242421050:AS-TRANSIT' (#54) from Napsterbater-20200716/as-set into master

    Reviewed-on: https://git.dn42.dev/dn42/registry/pulls/54
    Reviewed-by: schema-checker <schema-checker@noreply.dn42.us>
```

## crontab

You can setup a [cronjob][5] to check in with updates to the ROA files listed
above on regular intervals.

Currently the ROA files published here is refreshed every 10th hour if
updates has been made to the [DN42 registry][1].

## Misc statistics

- ROAs IPv4:  1263
- ROAs IPv6:  1022
- ROAs total: 2285

[0]: https://git.dn42.us/dn42/registry/commit/3a7ca794813b3dbdd3c435d95875a7d9c60bd30b
[1]: https://git.dn42.us/dn42/registry
[2]: https://github.com/NLnetLabs/routinator
[3]: https://github.com/cloudflare/gortr
[4]: https://tools.ietf.org/html/rfc8416
[5]: doc/crontab.md
[6]: https://github.com/cloudflare/gortr/#configure-filters-and-overrides-slurm

