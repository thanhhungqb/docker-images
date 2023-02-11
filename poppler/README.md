# Poppler tools

Usage:

    docker build -t pdfimages - < Dockerfile
    docker run --rm -v `pwd`/file.pdf:/file.pdf -v `pwd`:/out pdfimages pdfimages [opts] /file.pdf 
	
	