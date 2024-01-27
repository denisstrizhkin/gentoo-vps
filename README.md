# Gentoo VPS

after chroot

```console
# emerge-webrsync
# emerge -1 eselecty-repository dev-vcs/git
```

enable git repos

```console
# eselect repository enable gentoo
# eselect repository enable guru
# rm -rf /var/db/repos/gentoo
# emerge --sync
```

setup chezmoi

```console
# emerge -1 chezmoi
# chezmoi init --apply --verbose https://github.com/denisstrizhkin/gentoo-vps.git
# echo '@vps' > /var/lib/portage/world_sets
# emerge -avDNu @world
```
