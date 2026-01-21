## Welcome to my personal collection of datfiles I curate for various arcade, computer and console systems.  These datfiles are collections of file hashes and are used to verify legally owned copies of digital media. 

If these tools, dats, or archives save you time, consider supporting the work:

<a href="https://buymeacoffee.com/eggmansworld">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-orange.png" height="45" alt="Buy Me a Coffee">
</a>

## If you're here for the dats, you can find them in the Releases section. --->

For decades, I have enjoyed curating and creating collections of video game-related content. I exclusively use [RomVault](https://www.romvault.com) (aka RV) as my rom manager tool of choice to manage and audit my data. As a more advanced user of its features, I tend to push it to its limits (and sometimes beyond). RomVault gives me freedom to create more complex datfiles, such as deep hierarchical trees of folders and files which can even include zero-byte files and empty folders. Some of the datfiles presented here are more advanced than your garden variety flat-folder style dats that only contain archives.

To preserve some types of data, it might be best to store it as files, and treat everything including .zip and .7z archives as files. This comes in handy for sets that I may want to present as ready-to-play, or for preserving archives and files that contain system-sensitive timestamps (generic dat timestamps are not yet supported in RV). There are also file collections that would create archvies possibly in the in the hundreds of gigabytes in size, which become very difficult to manage effectively for most users of my dats. The main idea with my collections is to strike a balance between:
- preservation effectiveness (do the files presented need to be stored in a specific way?),
- curation quality (are the files and folders arranged in a sensible way that make it easy to navigate),
- usability (are the files going to be utilized by the user at times, such as in an emulator), and
- sanity when managing these files (don't intentionally make insanely large archives which become unweildly)

Below are some notes I have put together to assist users in understanding some of the more advanced and tricky features of managing their collections with RV. Hopefully I've been able to pass on the information in an understandable way without confusing anyone. If something does not make sense to you, please be sure to stop by the RomVault [Discord](https://discord.gg/fVJQPA8) and ask your questions!

# Archive Types Reviewed

When working with datfiles, you can modify the Archive Type of a folder by right-clicking on the folder and selecting "Set Dir Dat Settings". There are 4 modes you can set that affect how each folder is stored and processed:

<img width="384" height="103" alt="image" src="https://github.com/user-attachments/assets/a81f19fd-7e68-4b0f-ab23-887f025a944d" />

**Uncompressed**: This setting is only for standard datfiles and tells RomVault store the contents of the folder uncompressed instead of inside archives. Archives are stored as folders instead, one per archive. The contents of each archive will be stored inside the folder(s).
  NOTE: if you try to select this option on an Archive as File dat and use the "Override DAT" function, you will end up with warnings of "Trying to add a FileZip to a Dir". If you make this mistake, just click OK or press the ESC key for each warning that comes up until RV finishes parsing through the datfile (it might require numerous clicks to get through all the warnings). Go back and set the mode properly.

**Zip**: This is the default selection. All files in the dat are processed and contained within .zip archives. Zips are fully browsable by RomVault and the files inside can be processed as required by the datfile.  Uncompressed files are not allowed in this Archive Type. You can define the deterministic compression type of these zips to use either TorrentZip or ZStd.

**7Zip**: Same as Zip, only it uses 7-Zip archives to store files. Compression types for 7-Zip can be LZMA Solid/Non-Solid, or ZStd Solid/Non-Solid.

**Mixed (Archive as File)**: This setting is only for Mixed (Archive as File) datfiles. If the "fileonly" attribute is set in the header of the datfile, you do not need to set this mode as RV will process the dat correctly. If the fileonly mode is not present in the datfile header, then select this Archive Type mode to process all files, including archives, as simple files.  

Detailed info on archive types is available in the RV [Wiki](https://wiki.romvault.com/doku.php?id=archive_types).

# What is a "Mixed (Archive as File)" dat?

A "Mixed (Archive as File)" dat is to store every single file in the dat as files, including .zip and .7z archives. In this mode, Unlike the "Zip" and "7Zip" Archive Type settings, RomVault will not browse inside any .zip or .7z archives to see what files/folders they contain. It treats those archive files just like any non-compressed file. This is done to preserve the files and archives in their natural state. The only thing that RomVault can alter on files in and Archive as File dat is their naming.

When an Archive as File dat is created, a datfile author should be setting an attribute in the datfile header to indicate that its contents are to be processed in Archive as File mode.  When you load an an Archive as File dat in a text editor, you should see the following line in the <header> of the datfile:
<romvault forcepacking="fileonly" />

If the dat is created with the intent of hashing only files and this attribute is missing from the dat, the datter expects you to set the Archive Type manually. This isn't an ideal expectation as the structure of an Archive as File dat differs from a standard dat, and can really mess things up if you start compressing the files rather than storing them only as files.

# How to identify a Mixed (Archive as File) dat

RomVault currently does not visually identify that an Archive as File dat has been loaded (such as displaying an icon or different folder color). When you check the Dir Dat Settings of an Archive as File dat, it will display the Archive Type as "Zip", when in fact it is actually (invisibly) setup to be processed as an Archive as File dat. The RomVault author will need to update the RV code to add something to the Dat Tree to indicate an Archive as File dat (pending).

<img width="711" height="384" alt="image" src="https://github.com/user-attachments/assets/cea28139-fa69-4bf7-b1a6-ea48104d5383" />

A standard datfile that handles .zip and .7z internal archive contents would show the .zip and .7z archives in the Game List Grid, and when you highlight an archive file, the contents of those archives will be viewable in the Rom Details Grid.

<img width="644" height="235" alt="image" src="https://github.com/user-attachments/assets/92289685-0783-4a99-adba-cf1f89f7fe78" />

For ANY dat that is setup with "Mixed (Archive as File) mode (either by manually setting it via Set Dir Dat Settings, or contains the fileonly attribute in the dat header), you can identify by the way the contents are being displayed in the main RomVault window:
1. the Game List Grid (upper right box) will only show folders.  
2. The Rom Details Grid (lower right box) will only show files.  You may see various uncompressed file types listed, along with .zip and .7z listed as files. You will not be able to browse inside those archives in this view. 

For MY OWN Archive as File dats, as an extra measure of safety, I also enter "Mixed (Archive as File)" in the description line of a Archive as File dat. This description line will display as part of the dat folder name and is an easy visual identifier to aid in identifying an Archive as File dat. 

For example:

<img width="1007" height="384" alt="image" src="https://github.com/user-attachments/assets/851df0b5-e22d-4a8e-a9c5-6d2effd91027" />

# For Archive as File dats that contain the fileonly attribute: 
- do NOT make any Set Dir Dat Settings changes to the dat folder(s). RomVault will do this automatically. 
- if placing the Archive as File dats in a subfolder in the Dat Tree that also contain standard dats, ensure the parent folder(s) in the Tree Branch do not have the "Override Dat" setting enabled. If you do, RomVault will cause the dat(s) to use the parent folder's setting via inheritance and override the fileonly dat mode in the Archive as File dat(s). You'll notice this as the folders will be shown as zips in the Game List Grid, but the files in the Rom Details Grid will still show uncompressed.

<img width="893" height="161" alt="image" src="https://github.com/user-attachments/assets/de13efa6-1da0-445f-b26c-95063f3e2225" />

- To avoid this, it is likely best to keep the Archive as File dats in a separate branch in the Dat Tree with no parent inheritances.

# Where do I put files I want to use to rebuild into a standard dat or FileOnly dat?

You have 2 options:

## **ToSort (primary)**

- files and archives placed in your primary ToSort can be used to rebuild to any dat type.
- Zips and 7-Zips will be browsed and files inside will be hashed and accessible.
- Archive as File dats are able to access the files inside Zip and 7-Zip archives.
- After a find fixes operation completes, post-processing will recompress any archives inside the primary ToSort to TorrentZip or ZStd as required (depending on your top-level folder).

<img width="912" height="259" alt="image" src="https://github.com/user-attachments/assets/6576a827-e23c-4d99-80ca-bcb5d695cc94" />

## **ToSort (FileOnly)**
- RomVault recently added this feature to allow users to set any additional ToSort folder(s) in FileOnly mode (right-click > Set To FileOnly ToSort).
- This ToSort will show (FileOnly) after its name.
- Any files placed in a FileOnly ToSort will be treated as a file.
- Zips and 7-Zips will be treated as files, which means their contents are not browsed and hashed.
- After a find fixes operation completes, there is no post-processing tasks done on this folder and remaining files are left untouched.
- to remove the FileOnly setting on a ToSort, right-click and select "Clear FileOnly ToSort".

FileOnly ToSorts are perfect for adding content you absolutely DO NOT want modified in any way by RomVault.

<img width="929" height="355" alt="image" src="https://github.com/user-attachments/assets/e29bac89-e740-4688-9fca-bd30ee29d532" />

---

## Licensing

Original source code, scripts, tooling, and hand-authored documentation and
metadata in this repository are licensed under the MIT License.

Archived game data, binaries, firmware, media assets, and other third-party
materials are **not** covered by the MIT License and remain the property of
their respective copyright holders.

See the `LICENSE` and `NOTICE` files for full details and scope clarification.
