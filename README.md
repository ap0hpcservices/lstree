## Introduction

Display the directory tree via browser + the local web server or console.

# Usage

There are two versions to support PHP and python.

**PHP**

Put `lstree.php` into the directory you want to list it as a directory tree. Then use your browser to access it by the local server.

*NOTE*: the directory must be in http server document root directory.

**Python 3**

Put `lstree.py` into the **any** directory you want to list, and then run command:

    $ python lstree.py

Now you can get the directory tree via browser to go: `localhost:5000`

The directory tree example:

        /var/www/html/simple_site(d)
        |----login.php(f)
        |----test.php(f)
        |----wiki(d)
        |    |----readme.txt(f)
        |    |----resource(d)
        |    |----.htaccess(f)
        |    |----gamesConfig.php(f)
        |    |----.htpasswd(f)
        |    |----data(d)
        |         |----resource(d)
        |         |----users(d)
        |         |----blog(d)
        |              |----comments(d)
        |              |----articles(d)
        |
        |
        |
        |----index.php(f)
        |----game.php(f)

## More

You can configure the display details by modify the `LsTree` instance:

        setMode(mode)  			# 'html' or 'text' mode, default is html mode
        setLinkNum(linknum)  	# default link char repeat 4 times
        setLinkChar(linkchar)  	# default '-' is link char
        setDirMark(mark)  		# default 'd' is directory mark
        setFileMark(mark)  		# default 'f' is file mark
        setMarkDelimiter(delimiter)  # default is '()' for wrap 'f' and 'd'
        ls(dir)  				# specify the directory you want to display
        render(filename) 		# if you want write directory tree into a file, specify a filename
