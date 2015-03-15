The Virtual File System (VFS) combines multiple directory structures into a single view of the filesystem used to load [assets](Asset).

Search order:
  * Files in the active [mod](Mod) directory, if any
  * Data archives in the active [mod](Mod) directory, if any
  * Files in the application's base directory
  * Data archives in the application's base directory

# Base directory #
The base directory is usually located in the directory of the application EXE and named `base`. This location can be overridden in the engine configuration.

# Data archives #
The data archives provide a a way to combine the entire game content (maps, scripts, models, textures, ...) into a few large files. This simplifies installation and updating and also reduces the likelihood of users accidentally modifying the content.

The data archives are normal ZIP archives internally with the file ending `.pk5` instead of `.zip`. They should be stored in uncompressed form to speed up loading processes.