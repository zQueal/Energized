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

The build method is the same for each list.

_Note: The file locations in the script are relative, meaning you MUST compile from the source directory or the script will fail._

--------------------------------

# Using EnergizedProtection

You may also use the backup feature of the script, though it's a bit combersome.

1. Compile the list you want to use and rename `hosts` to `hosts-backup`
2. `gzip` it using `7-zip`;

> 7z c hosts-backup.gz ./hosts-backup

3. Transfer `hosts-backup.gz` to your phones storage at `/sdcard/EnergizedProtection/hosts-backup.gz`
4. Use the script menu option `rs` (restore) to restore the backup
5. Back on the main menu, make **another backup**
6. Restore **again** (yes, twice) using the backup you just made
7. Restart your phone

The number of domains being blocked still refuse to show up, but this seems to work fine.

# Using AdAway

1. Compile the list you want to use
2. Transfer the `hosts` file to your phone storage
3. Use AdAway to import the `hosts` file as a source
4. Update and apply
5. Restart your phone
