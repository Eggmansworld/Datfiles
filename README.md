## Welcome to my personal collection of datfiles I curate for various arcade, computer and console systems.

These datfiles are collections of file hashes used to verify and organize legally owned copies of digital media. The goal is not just to hash files for the sake of hashing them, but to present preservation-focused sets in a way that is practical to manage, sensible to browse, and appropriate to the type of content being preserved.

<img width="1536" height="645" alt="image" src="https://github.com/user-attachments/assets/b4559b22-2408-46d8-8cd0-c0c036330760" />

If these tools, dats, or archives save you time, consider supporting the work:

<a href="https://buymeacoffee.com/eggmansworld">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-orange.png" height="45" alt="Buy Me a Coffee">
</a>

## If you're here for the dats, you can find them in the Releases section, or click a link below:
- [Arcade Ambience Project](https://github.com/Eggmansworld/Datfiles/releases/tag/arcadeambience)
- [BlueMaxima.org Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/bluemaxima)
- [C64 Ultimate Tape Archive](https://github.com/Eggmansworld/Datfiles/releases/tag/c64ultimatetape)
- [Digitoxin's PC Game Preservation Project](https://github.com/Eggmansworld/Datfiles/releases/tag/digitoxin)
- [eXo Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/exo)
- [Fruit Machines, The Private Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/fruitmachines)
- [GoodTools Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/goodtools)
- [High Voltage SID Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/hvsc)
- [iPod Clickwheel Games Preservation Project](https://github.com/Eggmansworld/Datfiles/releases/tag/ipodclickwheel)
- [Laserdisc Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/laserdisc)
- [Pinball PC Games Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/pinballpc)
- [Project EGG Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/projectegg)
- [RPG Maker Archive](https://github.com/Eggmansworld/Datfiles/releases/tag/rpgmaker)
- [Sega ALL.Net Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/segaalldotnet)
- [Sharp X68000 Project](https://github.com/Eggmansworld/Datfiles/releases/tag/sharpx68000)
- [TeknoParrot Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/teknoparrot)
- The Most Complete Amiibo Set - no longer datted by me, visit [Nintendo Library](https://nintendolibrary.com) to download the latest Amiibo dat
- [Touhou Project Collection](https://github.com/Eggmansworld/Datfiles/releases/tag/touhou)
- [VIC20 Ultimate Tape Archive](https://github.com/Eggmansworld/Datfiles/releases/tag/vic20ultimatetape)

## The following collections have their own repositories:
- [DUSTBUNNiES Collection](https://github.com/Eggmansworld/DUSTBUNNiES)
- [Eggman’s Arcade Repository](https://github.com/Eggmansworld/Eggmans-Arcade-Repository)

---

## What this repository is for

For decades, I have enjoyed curating and building collections of video game-related content. This repository is where I publish the datfiles I use to organize, verify, and preserve many of those collections.

Some of these sets are simple and conventional. Others are deliberately more advanced and make use of features that many ROM managers either do not support well, or do not support at all. A lot of my dats are designed around real-world preservation needs rather than around the older expectation that every set should be a flat list of archives in one folder.

That is why this repo is built around **RomVault**.

---

## Why I use RomVault

I exclusively use [RomVault](https://www.romvault.com) (also called **RV**) as my ROM manager of choice.

RomVault gives me the flexibility to build and manage collections that go beyond basic archive-only sets. Depending on the needs of the material, a collection may need to preserve things such as:

- deeply nested folder structures
- uncompressed files
- ZIP or 7z archives treated as normal files
- zero-byte files
- empty folders
- content that is meant to stay in a ready-to-use layout instead of being repacked into giant archives

Those are all situations where RomVault is especially useful.

A lot of the dats here are not “garden variety” flat-folder dats. Some are straightforward archive sets, but others are structured more like real software collections or preservation trees. In those cases, the way the files are stored matters just as much as the hashes themselves.

So when I design a collection, I usually try to balance four things:

- **preservation effectiveness**  
  Does the content need to stay in a particular structure or form in order to preserve it properly?

- **curation quality**  
  Are the files and folders arranged in a way that makes sense to browse and understand?

- **usability**  
  Is this a collection people may actually want to extract, inspect, mount, or run in an emulator?

- **sanity when managing it**  
  Do not build intentionally absurd archive layouts that become a nightmare for normal users to handle.

That balance is the main reason my dats sometimes behave differently from what users may expect from more traditional ROM sets.

If something in this README still does not make sense, I strongly recommend stopping by the RomVault [Discord](https://discord.gg/fVJQPA8) and asking questions there.

---

## Table of Contents

- [What this repository is for](#what-this-repository-is-for)
- [Why I use RomVault](#why-i-use-romvault)
- [How my datfiles and collections are generally structured](#how-my-datfiles-and-collections-are-generally-structured)
- [Archive Types in RomVault](#archive-types-in-romvault)
- [What is a "Mixed (Archive as File)" dat?](#what-is-a-mixed-archive-as-file-dat)
- [How to identify a Mixed (Archive as File) dat](#how-to-identify-a-mixed-archive-as-file-dat)
- [Important rules for fileonly / Archive as File dats](#important-rules-for-fileonly--archive-as-file-dats)
- [Where to put files you want to rebuild from](#where-to-put-files-you-want-to-rebuild-from)
- [Licensing](#licensing)
- [Credits](#credits)

---

## How my datfiles and collections are generally structured

Not every collection should be stored the same way.

Some content is best handled as normal archive-based dats, where RomVault can look inside ZIPs or 7z files and rebuild individual files as needed.

Other content is better preserved in a more natural state, where the original files, folders, ZIPs, and 7z archives remain exactly as they were distributed. This is especially useful for things such as:

- pre-configured “ready-to-play” sets
- software collections with important folder structure
- collections containing archives you do **not** want RomVault to unpack and reinterpret
- content with timestamp-sensitive files, where generic dat timestamp support is not available in RomVault
- sets that would become unwieldy if packed into enormous archives

That is why you will see different storage approaches across my dats.

Broadly speaking, my collections tend to fall into one of these categories:

### 1. Standard archive-based dats
These are the traditional-style dats. RomVault can browse inside the archives, hash the internal files, and rebuild the set normally.

### 2. Uncompressed structured dats
These are still standard dats, but the content is meant to live as folders and files rather than being stored inside archives.

### 3. Mixed / Archive as File dats
These are designed so that **everything** is treated as a file, including ZIPs and 7z archives. RomVault does not browse inside the archives at all. This is the mode I use when the archive file itself is part of what is being preserved.

If you keep that distinction in mind, a lot of the “why is this dat behaving like this?” confusion tends to go away.

---

## Archive Types in RomVault

When working with datfiles in RomVault, you can modify the archive behavior of a folder by right-clicking the folder and selecting **Set Dir Dat Settings**.

There are four archive modes you can work with:

<img width="384" height="103" alt="image" src="https://github.com/user-attachments/assets/a81f19fd-7e68-4b0f-ab23-887f025a944d" />

### Uncompressed
This is for standard datfiles where you want the contents stored as normal files and folders instead of inside archives.

If the dat expects archives, RomVault will instead store each archive as a folder and place the archive contents inside that folder.

**Important note:** if you accidentally apply this to an Archive as File dat and use **Override DAT**, RomVault may throw repeated warnings such as:

`Trying to add a FileZip to a Dir`

If that happens, just dismiss the warnings until parsing finishes, then go back and set the archive mode correctly.

### Zip
This is the default mode for many standard dats.

All files are stored inside `.zip` archives. RomVault can browse those ZIPs, hash the files inside them, and rebuild content normally. Uncompressed loose files are not allowed in this mode.

For deterministic ZIP compression, you can use either:

- **TorrentZip**
- **ZStd**

### 7Zip
This behaves similarly to Zip mode, except the content is stored in `.7z` archives instead.

Supported compression styles include:

- **LZMA Solid**
- **LZMA Non-Solid**
- **ZStd Solid**
- **ZStd Non-Solid**

### Mixed (Archive as File)
This is the special mode used for Archive as File / fileonly-style dats.

In this mode, RomVault treats **all files as files**, including `.zip` and `.7z` files. It does not browse inside them.

If the dat header includes the fileonly marker, RomVault should process it automatically without you needing to set this manually.

Detailed archive-type documentation is also available in the RomVault [Wiki](https://wiki.romvault.com/doku.php?id=archive_types).

---

## What is a "Mixed (Archive as File)" dat?

A **Mixed (Archive as File)** dat is a dat where every file is meant to stay a file, including archives.

That means:

- `.zip` files are treated as files
- `.7z` files are treated as files
- RomVault does **not** inspect their internal contents
- the archive file itself is what gets preserved and hashed

This is very different from standard **Zip** or **7Zip** dat behavior, where RomVault opens the archive and works with the files inside it.

Archive as File mode is useful when you want to preserve content in the same state it naturally exists in. For example:

- pre-built software packs
- collections distributed as ZIP bundles
- sets where the archive itself matters
- content you do not want recompressed or reinterpreted internally

In this mode, RomVault can still rename files if needed, but it does not get to treat the inside of an archive as rebuildable content.

### The fileonly header flag

If a dat is intentionally built for Archive as File mode, the dat header should contain this line:

```xml
<romvault forcepacking="fileonly" />
```

If that attribute is present, RomVault knows the dat is supposed to behave in fileonly mode.

If the dat author built a fileonly-style dat but did **not** include that line, then the user is expected to set the mode manually. That is not ideal, because the structure of a fileonly dat is fundamentally different from a standard one, and it is easy for users to mis-handle it.

---

## How to identify a Mixed (Archive as File) dat

At the moment, RomVault does **not** give Archive as File dats a strong visual identifier in the dat tree.

For example, if you look at **Dir Dat Settings**, RomVault may still show the Archive Type as **Zip**, even though the dat is effectively being processed in Archive as File mode behind the scenes.

<img width="711" height="384" alt="image" src="https://github.com/user-attachments/assets/cea28139-fa69-4bf7-b1a6-ea48104d5383" />

So how do you tell?

### Standard archive-based dat behavior
With a normal dat, ZIP and 7z archives appear in the **Game List Grid**, and when you highlight one, you can browse its contents in the **Rom Details Grid**.

<img width="644" height="235" alt="image" src="https://github.com/user-attachments/assets/92289685-0783-4a99-adba-cf1f89f7fe78" />

### Archive as File behavior
With a Mixed / Archive as File dat:

1. the **Game List Grid** (upper-right pane) will show only folders  
2. the **Rom Details Grid** (lower-right pane) will show files only  
3. ZIP and 7z files appear as files, not as browsable archives  
4. you will not be able to inspect their internal contents from this view

## For my own Archive as File dats, I add **“Mixed (Archive as File)”** into the description line as an extra safety cue, so the dat folder name itself gives you a visual hint about what kind of dat you are dealing with.

For example:

<img width="1007" height="384" alt="image" src="https://github.com/user-attachments/assets/851df0b5-e22d-4a8e-a9c5-6d2effd91027" />

---

## Important rules for fileonly / Archive as File dats

For Archive as File dats that already contain the `fileonly` attribute:

- **if you don't want to see a whole bunch of files in folders, set your "DAT Rule Settings" Single Archive to "Do not use subdirs for sets".**
- If these dats are placed under parent folders that use **Override DAT**, be careful. Parent inheritance can override the child dat behavior and break the expected fileonly processing.
- If that happens, you may notice odd mixed behavior, such as ZIPs appearing in the Game List Grid while the Rom Details Grid still shows loose files.

<img width="893" height="161" alt="image" src="https://github.com/user-attachments/assets/de13efa6-1da0-445f-b26c-95063f3e2225" />

### Best practice
The safest approach is usually to keep Archive as File dats in their **own separate branch** of the Dat Tree, away from parent folder inheritance settings.

That avoids a lot of accidental misconfiguration.

---

## Where to put files you want to rebuild from

If you want RomVault to rebuild files into either a standard dat or a fileonly dat, you generally have two choices.

## ToSort (primary)

This is the normal, main ToSort.

Use it when you want maximum rebuild flexibility.

### What it does
- files and archives placed here can rebuild into any dat type
- ZIP and 7z archives will be browsed internally
- files inside those archives can be hashed and used
- Archive as File dats can still access the contents inside ZIP and 7z archives that are placed here
- after **Find Fixes**, RomVault may recompress remaining material based on the rules of your top-level folder

<img width="912" height="259" alt="image" src="https://github.com/user-attachments/assets/6576a827-e23c-4d99-80ca-bcb5d695cc94" />

In short, this is the flexible, “let RomVault do its thing” rebuild area.

## ToSort (FileOnly)

RomVault also supports **FileOnly ToSort** folders.

You can create one by right-clicking a ToSort and selecting **Set To FileOnly ToSort**.

### What it does
- the ToSort will display **(FileOnly)** after its name
- all files placed there are treated as files
- ZIP and 7z archives remain files and are **not** browsed internally
- after **Find Fixes**, RomVault does **not** perform post-processing on the leftovers
- the remaining files stay untouched

To remove the FileOnly flag later, right-click and select **Clear FileOnly ToSort**.

FileOnly ToSort folders are ideal when you have material that you absolutely do **not** want RomVault to modify, unpack, reinterpret, or recompress.

<img width="929" height="355" alt="image" src="https://github.com/user-attachments/assets/e29bac89-e740-4688-9fca-bd30ee29d532" />

---

## Licensing

Original source code, scripts, tooling, and hand-authored documentation and
metadata in this repository are licensed under the MIT License.

Archived game data, binaries, firmware, media assets, and other third-party
materials are **not** covered by the MIT License and remain the property of
their respective copyright holders.

See the `LICENSE` and `NOTICE` files for full details and scope clarification.

---

## Credits

Created for the preservation community by Eggman, with Claude’s help turning ideas into code.

*Made with ❤️ for the retro game preservation community.*
