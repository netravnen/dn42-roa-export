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
instead (e.g. `-slurm export_rfc8416_dn42.json`) as a command-line parameter.

## [Last merge commit][0] at [dn42 registry][1]

```
Commit 2507665cb812eebb079257b5aed9fd183ea1d7cd
Merge: 6914431f6 278aefd5f
Date:   2021-02-24 20:13:35 +0000

    Merge pull request 'Registerd DMail and UnknownTS domains' (#552) from zane_reick-20210224/register-dns into master
```

## crontab

You can setup a [cronjob][5] to check in with updates to the ROA files listed
above on regular intervals.

Currently the ROA files published here is refreshed every 10th hour if
updates has been made to the [DN42 registry][1].

## Misc statistics

- ROAs IPv4:  1416
- ROAs IPv6:  1203
- ROAs total: 2619

[0]: https://git.dn42.dev/dn42/registry/commit/2507665cb812eebb079257b5aed9fd183ea1d7cd
[1]: https://git.dn42.dev/dn42/registry
[2]: https://github.com/NLnetLabs/routinator
[3]: https://github.com/cloudflare/gortr
[4]: https://tools.ietf.org/html/rfc8416
[5]: doc/crontab.md
[6]: https://github.com/cloudflare/gortr/#configure-filters-and-overrides-slurm

