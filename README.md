# Matew - Make Album The Easy Way

Matew is a valid HTML/CSS generator for static image albums. It supports retrieving information from EXIF cameras and includes customizable options like character set encoding. Albums may contain sub albums, and the appearance of an album can be fully personalized and customized choosing a CSS style file, setting names and descriptions of albums and individual images.

## Features

* Albums can contain sub albums: The album can have a tree structure.
* Automatical generation of a thumbnail and of scaled images for each image.
* EXIF information: Use of EXIF data structure found on some image files (usually, those produced by digital cameras and image's softwares manipulation) to fill automatically some fields (camera model, date and time for example).
* Easy to use matew-wizard script to set the configuration file. Some of the fields it handles are:
** Character encoding for HTML generation, including UTF-8 (Unicode) support by default.
** Generated album appearance is customizable by choosing a default CSS style files or editing your own one.
** Internationalization (generation of album in different languages) by choosing a language file. Current supported languages are english, brazilian portuguese, italian, sweden and croatian.
** Support for a standard link to an external file.
** Thumbnails per page: You can choose how many thumbnails per column and per line the album will visualize.
* Three description fields (name, description and image identifier) can be associated with each album (in text or HTML format). You can easily customize these fields.

## Usage

I advice you to login as root and install the script. By the way if you just want to try the script before installing it onto the system do as follows:

1. Unpack the source into your home directory:
```
# tar xfz matew.tar.gz
```
or
```
# unzip matew.zip
```
2. Run `matew-wizard` to setup the configuration file:
```
# cd ./matew/src
# ./matew-wizard
```
Note: Read the instruction carefully
3. Finally run matew:
```
# ./matew <source path> <target path>
```
Note: `<source path>` is the directory where the images are stored in. `<target path>` is the directory where you want the album to be created. This path can be the same as the source path.
It's strongly reccomanded to run matew with the verbose flag at least the first time you run it:
```
# ./matew -v <source path> <target path>
```
This way you can see exactly what the script is doing every time.
4. Read the matew help usage for more details:
```
# ./matew -h
```
Note: The `-i` flag can be used to create the information files (album_description and image_descriptions). It is really useful the first you run matew on a certain `<source path>`. Then you can edit these files to setup album name, album description, album image identifier and a long description for one or more images. Later run matew without the -i flag. You will notice that now there are more information in the album output pages.

## Installation

To install the script login as root then, enter the unpacked matew directory and run the install script:

# cd ./matew
# ./install

This will put the script executable files into `/usr/bin`, language and style directories into `/etc/matew` and documentation files into `/usr/share/doc/matew`.

Now you can run matew from wherever you want. For further information about the usage read the [[Usage]] paragraph.

## Dependencies

[ImageMagick](http://www.imagemagick.org) for convert and identify command line tools.

## License

matew is released under the terms of the [General Public License v2](http://www.gnu.org/licenses/gpl-2.0.html).
