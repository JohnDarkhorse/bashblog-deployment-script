#! /bin/bash
##
## Author: J. Darkhorse
## License: MIT
##
## This script is meant to be run AFTER you create a blog post with bashblog and are ready to publish it.
##
## Please change all variables to match your setup
##
## Makes sure we're in our blog build directory
cd /psth/to/blog/build/dir/ &&

## bashblog ( as of build 89780c3 ) offers a "bb.sh edit -f" option 
## which allows a user to edit the full HTML code of an existing blog post.  
##
## Unfortunately, at the next "bb.sh rebuild", many changes made using 
## the "bb.sh edit -f" mode will be nuked.
##
## Once you get your blog post looking the way you want it to with "bb.sh edit -f", 
## you must move it to another directory so it's not nuked
##
## List any blog.html files that are in your "safe space" below so their 
## munged/nuked versions created by the next "bb.sh rebuild" aren't propogated to your 
## live site, overwriting your "good" version(s)
##
## You will need to list all your customized blog files by name here ( your "good" versions 
## are in "./safespace", right? )
rm ./special-blog-file-01.html || true &&
rm ./special-blog-file-02.html || true &&

## moves our specially decorated files to the web-facing blog directory
/bin/cp ./safespace/*.html /path/to/public_html/blogdir/ &&

## moves .html files to our blog directory
/bin/cp *.html /path/to/public_html/blogdir/ &&

## moves .css files to our blog directory
/bin/cp *.css /path/to/public_html/blogdir/ &&

## moves .rss files to our blog directory
/bin/cp *.rss /path/to/public_html/blogdir/ &&

## moves our specially decorated files back into our blog build directory 
## so bb.sh can properly render our index, tag_pages and RSS feed at next "bb.sh rebuild"
/bin/cp ./safespace/*.html /psth/to/blog/build/dir/
