# Latex tools

## Miktex

From git@github.com:MiKTeX/docker-miktex.git


	cd docker-miktex/
	docker build --network=host -t miktex .
	
run

	% make volumn miktex for reuse
	docker volume create --name miktex
	docker run --network=host -ti -v miktex:/miktex/.miktex -v pwd:/miktex/work miktex pdflatex main.tex
 
# Textlive tools

? not yet

Usage:

	docker build -t textlive .
    docker run -v `pwd`:/source textlive [filename].tex