# Files
## Root Directory `/`
### `bin`
* All the commands and binaries
### `etc`
* Configuration files
### `dev`
* Devices
### `temp`
* Scratch space
* Temporary
### `var`
* Program data

## file metadata
### `inode`
* Metadata for a file/directory
* Not including the name

## Linking
### Hardlink `ln <file> <linkname>`
* A direct link to the exact file
* cannot hardlink across partitions

### Symlink `ln -s <file> <linkname>`
* creating another file that points to the linked file
* can softlink across partitions

## Permissions
### Components
* Owner
* Group
* Other

### Permissions
* Read
	* 4
	* 100
* Write
	* 2
	* 010
* Execute
	* 1
	* 001