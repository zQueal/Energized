# Requirements

 * bash
 * git
 * jq

# Build Steps

1. Clone the Energized Block repository;

> git clone https://github.com/EnergizedProtection/block

2. Download / update the source list;

> cd block/assets/sources; sh filter.sh

You'll be asked to identify your whitelist directory;

> [+] Enter Whitelist Directory:

_Note: You'll also be warned about not having `table.php`, which is totally fine._

> [...]
> ! Done Filtering.

3. Compile the list you want;

_Note: We'll use the `blu` list as an example;_

> cd block/blu; sh build.sh

```sh
!    _____  _________  _____________  _______
!   / __/ |/ / __/ _ \/ ___/  _/_  / / __/ _ \
!  / _// ,  / _// , _/ (_ // /  / /_/ _// // /
! /___/_/|_/___/_/|_|\___/___/ /___/___/____/
!
!    P   R   O   T   E   C   T   I   O   N
! --------------------------------------------
! B U I L D I N G  P A C K S
! --------------------------------------------
! Pack: Energized Blu Protection
! Domains: 319,640
! Version: 22.12.350
! --------------------------------------------
! Building hosts Format
! Building hosts text Format
! Building hosts ipv6 Format
! Building domain list Format
! Building adblock filter Format
! Building DNSMasq Format
! Building DNSMasq ipv6 Format
! Building unbound Format
! Building rpz Format
! Building one-line Format
! Building hosts gzip Format
! Building chromium ruleset Format
! --------------------------------------------
! DONE BUILDING PACK & FORMATS.
! --------------------------------------------
```

__That's it.__ The compiled host file will be located at;

> block/blu/formats/hosts

Simply move it to your device (phone) storage and use a third party adblocker like AdAway to load the list from your devices' storage as a file. Apply the rules, and restart.

The build method is the same for each list.

_Note: The file locations in the script are relative, meaning you MUST compile from the source directory or the script will fail._
