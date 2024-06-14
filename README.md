Prologue
--

If you're trying to build VyOS ISO image with the usual way you may see following errors:

```
E: Failed to fetch http://dev.packages.vyos.net/repositories/equuleus/dists/equuleus/InRelease  403  Forbidden [IP: 104.18.30.79 443]
E: The repository 'http://dev.packages.vyos.net/repositories/equuleus equuleus InRelease' is not signed.
E: Failed to fetch http://dev.packages.vyos.net/repositories/sagitta/dists/sagitta/InRelease  403  Forbidden [IP: 104.18.30.79 443]
E: The repository 'http://dev.packages.vyos.net/repositories/sagitta sagitta InRelease' is not signed.
```

You may also see `Sorry, you have been blocked` if you try to visit these links, but you aren't blocked - everyone
is blocked. This is due to [change in VyOS policy](https://blog.vyos.io/community-contributors-userbase-and-lts-builds)
where they don't offer their `dev.packages.vyos.net/repositories` for public anymore. This change applies only to
stable branches (like 1.3 equuleus/1.4 sagitta), you can still build current/development branch as usual with
`dev.packages.vyos.net/repositories`.

# VyOS ISO Automation Build

Automate build VyOS  v1.3 LTS Release and v1.4 LTS Release ISO files.



## About this repository

Used the unofficial build script provided by VyOS [https://github.com/ashimov/vyos-build](https://github.com/ashimov/vyos-build).

## Github Action workflow files

Github Action automate the build process and save you some times.


[vyos-v1.4-lts-release.yml](.github/workflows/vyos-v1.4-lts-release.yml)

For VyOs v1.4 LTS release, action trigger on schedule every day. ISO file can be found in the Action Artifacts section.

You can edit the workflow files to modify the trigger conditions to suit your needs.
