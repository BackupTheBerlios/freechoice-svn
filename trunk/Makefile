A01= 01_intro
A02= 02_mercado
A02a1= 02a_competencia_ta
A02a2= 02a_competencia_silice
A03= 03_estrategia_mision
A04= 04_factores_criticos
A05= 05_foda
A06= 06_planmartk
A07= 07_fact_tecnica
A08= 08_gerencia

all:	
	rm -f *.html
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A01}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A02}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A02a1}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A02a2}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A03}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A04}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A05}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A06}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A07}.txt
	asciidoc.py --attribute=encoding=ISO-8859-1 ${A08}.txt
	sed '/^<\/body>/d' ${A01}.html |  sed '/^<\/html>/d' > all.html
	sed '1,259d' ${A02}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A02a1}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A02a2}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A03}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A04}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A05}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A06}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A07}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	sed '1,259d' ${A08}.html | sed '/^<\/body>/d' | sed '/^<\/html>/d' >> all.html
	echo '</body></html>' >> all.html
	firefox all.html &

clean:
	rm -rf *~ *.html *.doc
