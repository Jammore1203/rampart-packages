# rampart-packages

The signed pacman repository for [Rampart](https://github.com/Jammore1203/rampart),
a hardened Arch Linux distribution. Installed Rampart systems update their
own packages (`rampart`, `rampart-keyring`, `rampart-hardening` and the
Parapet desktop, `parapet-git`) from here; everything else comes from Arch's
mirrors.

The repository is the [`x86_64` release](https://github.com/Jammore1203/rampart-packages/releases/tag/x86_64):
each package, and the database, is a release asset with its detached
signature. pacman reads it as:

```ini
[rampart]
SigLevel = Required
Server = https://github.com/Jammore1203/rampart-packages/releases/download/x86_64
```

Rampart installs this as `/etc/pacman.d/rampart.conf` (from the `rampart`
package), included from `/etc/pacman.conf`.

Every package and the database are signed with Rampart's package signing
key, `D4EE3DA274C20536AD07C2D38C61A87F48865C9F`, which the `rampart-keyring`
package adds to pacman's keyring.

The packages are published by `dev/publish` in the Rampart repository. There
is nothing else in this repository.
