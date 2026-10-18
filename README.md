# nfs-blackbox-assets

Large mod files the [NFS Black Box PS5](https://github.com/lavavex/nfs-blackbox-ps5) apps
download, as GitHub release assets. Each app's install plan pins every file here by size and
SHA-256, and a file that doesn't match is refused. Nothing here is a game: the apps need the
player's own copy.

## `nfsmw-x360-1`: Most Wanted (2005), the Xbox 360 look

Downloaded only when the player turns on the Xbox 360 look.

| File | Size | SHA-256 | Holds |
| --- | ---: | --- | --- |
| `nfsmw-x360-stuff-pack-4.2.zip` | 1,495,687,165 | `885d28e1ee3931d13949617750158660ae2213a1813adc663fef81bf729f1f3d` | the Xbox 360 Stuff Pack 4.2, 130 files, without its glass shader |
| `nfsmw-x360-movies-1.zip` | 1,831,439,018 | `4678a43553c887eb27283b3e822d29474a5ebe4e84421551cd351337d440e231` | the Xbox 360 Converted Movies, 30 of 33 |
| `nfsmw-x360-movies-2.zip` | 315,890,574 | `b43b63bdf06e1c599bfd5f6928913dd01443ea4efbcf7379da3bb31eea7c1763` | the Xbox 360 Converted Movies, the other 3 |

Where they come from:

- **Xbox 360 Stuff Pack 4.2**: [nfsmods.xyz/mod/1200](https://nfsmods.xyz/mod/1200), the
  "easy installation" files from its Google Drive folder.
- **Xbox 360 Converted Movies**: [nfsmods.xyz/mod/3006](https://nfsmods.xyz/mod/3006), from
  its Google Drive folder.

Google Drive isn't a steady download address for an app (big files go through a
confirmation page and download quotas), so the files are repacked here unchanged: stored
zips (no compression), entries in sorted order with fixed times, made by
`tools/make-x360-assets.py` in the project repo. Every file in them is listed with its size
and SHA-256 in `profiles/nfsmw/x360-assets.json` there, and two runs give the same bytes.
The movies are split in two to keep each file under 2 GB.

## Credits

All of this is the work of the mods' authors, credited on their nfsmods.xyz pages; it is
repacked only so the apps can download it over HTTPS with pinned hashes. If you made one of
these and want it changed or taken down, open an issue.
