A01= 01_intro
A02= 02_mercado
A02a1= 02a_competencia_ta
A02a2= 02a_competencia_silice
A03= 03_estrategia_mision
A04= 04_factores_criticos
A05= 05_foda

all:	
	rm -f *.html
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A01}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A02}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A02a1}.txt
	#asciidoc.py --attribute=encoding=ISO-8859-1 ${A02a2}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A03}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A04}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A05}.txt
	cat ${A01}.html > all.html
	cat ${A02}.html >> all.html
	cat ${A02a1}.html >> all.html
	#cat ${A02a2}.html >> all.html
	cat ${A03}.html >> all.html
	cat ${A04}.html >> all.html
	cat ${A05}.html >> all.html
	firefox all.html

replace:
	replace á a -- *.txt *.txt
	replace é e -- *.txt *.txt
	replace í i -- *.txt *.txt
	replace ó o -- *.txt *.txt
	replace ú u -- *.txt *.txt


clean:
	rm -rf *~ *.html
