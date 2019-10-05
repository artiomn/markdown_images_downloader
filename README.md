# Markdown articles image links fixer

Simple script to download images and replace image links in markdown documents.
I.e. you have Markdown document with HTTP links.
This script will find all links to images, download images and fix links in the document.


## Usage

Syntax:

```
./images_extractor.py [-h] [-s SKIP_LIST] article_file_path

positional arguments:
  article_file_path     an integer for the accumulator

optional arguments:
  -h, --help            show this help message and exit
  -s SKIP_LIST, --skip-list SKIP_LIST
                        skip URL's from the comma-separated list (or file with a leading '@')
  -a, --skip-all-incorrect
                        skip all incorrect images
```

Example:

```
./images_extractor.py nc-1-zfs/article.md
```

Example 2:

```
./images_extractor.py not-nas/sov/article.md -s "http://www.ossec.net/_images/ossec-arch.jpg" -a
```


## Warning

This tool will download only images, used Markdown syntax to link.
Images, linked with HTML "\<img\>" tag will not be downloaded!

