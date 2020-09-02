Este projeto é uma adaptação para o ambiente R Markdown utilizando a ferramenta bookdown combinando o modelo canônico de trabalho acadêmicos da \abnTeX e a adapatação para UFPR realizada por Emilio E Kawamura.

A iniciativas originais podem ser encontradas em:

https://www.abntex.net.br
README: 
                            abnTeX2  
                Type�set technical and scientific 
             Brazilian documents based on ABNT rules
             
-----------------------------------------------------------------

This is the README file for abntex2 class and abntex2cite package. 
Please read the license information at the end of this file.

The abntex2 class and the abntex2cite package are intended to 
assist the preparation of technical and scientific documents 
(like thesis, articles, research projects and other 
academic papers) based on ABNT (Associação Brasileira de Normas 
Técnicas) rules used in Brazil.

The latest version of abnTeX2 is v-1.9.7 (2018/11/24).

SUMMARY
-----------------------------------------------------------------

  This file consists of the following sections:
  
  . Change history
  . Installation
  . Documentation
  . Copying and modification
  . Help

CHANGE HISTORY
-----------------------------------------------------------------
  2018/11/24 - v1.9.7
    . added compliance to ABNT NBR 6022:2018 for article template
    . added \tituloestrangeiro (title in foreign language) for article template
    . fixed various spelling errors and improvements
     (thanks to @edusantana @apinheiro @ycherem) 
    . added example of frame (Quadro) in abntex2-modelo-trabalho-academico.tex 
    (thanks to @edusantana)

  2016/02/26 - v1.9.6.1
    . fixed warning message in the english TOC
  
  2016/02/26 - v1.9.6
    . added compliance to ABNT NBR 10719:2015
    . added \ABNTEXcaptiondelim command
    . added documentation for superscript citations 
    . changed caption's separator to enddash, in accordance to ABNT NBR 14724:2011
    . removed implementation of multifootnote, once memoir has "," as
      default value for \multfootsep 
    . fixed invalid dependence on relsize package 
    . fixed footnote mark size for footmarkers more than 1 character longer
    . fixed caption delimiter: 
      \ABNTEXcaptiondelim: \textendash for captions 
      \ABNTEXcaptionfontedelim: colon for source (fonte)
    
  2015/04/28 - v1.9.5
    . fixed abntex2cite.pdf bibliography errors
    . normalized the authorship of the documents  

  2015/04/26 - v1.9.4
    . changed url references to the new domain: www.abntex.net.br (#143)
    . fixed differences in .bst files (#144) 
    . added back the "calc" package in order to solve conflicts 
      with chapter configurations (#140)

  2015/01/26 - v1.9.3
    . added \selectlanguage at begin{document} in all examples
    . added a minimal pandoc template, making it possible to generate abntex2 
      documents from markdown files
    . changed sumario=abnt-6027-2012 option: now the "References" chapter label
      is printed in uppercase in TOC
    . changed deprecated command \glossarystyle to \setglossarystyle  
    . changed abntex2.tex: 
      \counterwithout replaced by \counterwithin
      added several improvements 
    . changed .sty files to print "volume" field at @book bib entries 
    . changed example of "Ficha catalográfica"
    . changed default implementation of \imprimircapa
    . changed default value for \ABNTEXsignskip from 1cm to 0.7cm
    . removed "calc" package dependency in order to solve conflicts 
      with "external" tikz library
    . removed change history from source files

  2014/01/26 - v1.9.2
    . fixed "undefined control sequence. l.100 \settocpreprocessor ...": abntex2.cls
      now loads sumario=tradicional by default when memoir command \settocpreprocessor
      is not present (\settocpreprocessor was added in memoir {v3.6k}{2012/09/18}, TexLive 2013)
    . changed default article margins from 4cm to 3cm

  2013/12/26 - v1.9.1
    . minor fix errors in sumario=tradicional option
    . changed the presentation example name to 'Modelo de apresentação de
      slides com Beamer e abnTeX2'
    . added escape for '%', '#' and '_' characters in URL of bibliography references  
    . added information about "url packages" to abntex2cite.tex documentation
    . changed configurations in Table of Contents when option 
      abnt-6027-2012 is active. Now the chapter entry is in upper case, and
      the others entries has different formats as well
    . changed implementation of \phantompart: the macro adds some spacing in TOC
      even whether sumario=abnt-6027-2012 is not active  
    . changed implementation of "citacao" environment: now it uses
      \ABNTEXfontereduzida instead of \ footnotesize
    . Replaced ~--~ by ~\textendash~ in abntex2.cls class  

  2013/10/26 - v1.9
    . added customizations of table of contents in compliance to ABNT NBR 6027:2012
      (class option sumario=abnt-6027-2012 and sumario=tradicional) 
    . added macro \phantompart that helps control TOC and bookmark  
    . added microtype package to examples and documentation files
    . added a fifth level on text structure (use \paragraph as a subsubsubsection)
    . added new example of bibliography reference in abntex2cite (key hamada2008)
    . added new Makefile for Linux/POSIX based systems that might be used in order
      to install or update abnTeX2 apart of TeXLive/CTAN packages from the 
      distribution: you might just download and install the last version of abnTeX2 
    . fixed url link for "https" addresses on .bst files
    . fixed scape of caracter "&" in urls on .bst files
    . fixed the layout of url if the option-package-url = url is used with the
      abntex2cite.sty. Without this insert the url was displayed without 
      delimiters '<' and '>'
    . fixed title printed with \imprimirtitle in title pages (\imprimircapa,
      folhaderostocontent and abntex2-modelo-trabalho-academico's folhadeaprovacao)  
    . fixed language of the date command (\imprimirdata)
    . fixed space between label and name separator ("--") greater than 9th 
      item of listings 
    . suppressed "before chapter skip" on items of listings 
      (\setlength\cftbeforechapterskip{0pt})  
    . removed useless cmap package from examples

  2013/08/26 - v1.8
    . added an example of book produced with abntex2
    . added an example of a beamer presentation produced with abntex2
    . added macros \IBGEtab, \fonte and \nota in order to meet table 
      formatting requirements from IBGE 
    . changed indentation, margins, paragraph spacing and further 
      improvements of abstract environment
    . changed the font size of name of tables and figures due to a 
      congruent interpretation of ABNT NBR 14724:2011 and IBGE rules: 
      the font size of the name of tables and figures must be the same 
      of the text. The font size of sources and notes are keep the 
      same: a smaller and uniform one. 
    . fixed article model in compliance to ABNT NBR 6022:2003. 
    . fixed definition of chapternamenumlength in abnt chapter style 
    . added new general information in the documentation files

  2013/05/26 - v1.7.1
   . fixed bibliography format for article and journalpart

  2013/05/25 - v1.7
   . added an optional argument to the citacao environment: language.
     Now the quoted text in foreign language is automatically written in italics
     and the proper hyphenation system is selected. Use as: 
     \begin{citacao}[french]Texte français.\end{citacao}  
   . added new options chapter=TITLE, section=TITLE, subsection=TITLE and
     subsubsection=TITLE to the abntex2.cls class. These options change
     the sections and chapter titles to upper case;
   . added macro \footciteref to abntex2cite that prints a bibliography reference
     as a footnote in accordance to ABNT NBR 10520:2002 section 7.1.  
   . added xindy instructions in glossary model;
   . fixed abntex2cite's table 4: there was a line written twice;
   . changed class options declaration in all examples;   
   . fixed wrong \setsecheadstyle implementation that prevented font section be 
     changed as expected;
   . fixed bibliography style for @article and @journalpart caused by wrong
     implementation of iso-690-1987 option; 
   . fixed \apudonline compliance with section 7.1.3 from ABNT NBR 10520:2002: 
     the publication year of the main author now is printed;
   . fixed single spacing before chapters;
   . review text of documentations;   
   . replaced abntex2-doc-abnt-6023-2000.bib file by abntex2-doc-abnt-6023.bib:
     the new file replaces numerical bibkeys by keys composed by author name and year. 
     This aims to turn the document's updates easier;
   . merged abntex2-doc-abnt-10520-2001.bib and abntex2-doc-abnt-10520-2002.bib files
     into abntex2-doc-abnt-10520.bib;    

  2013/04/30 - v1.6.1
   . fixed use of different languages on example and documentation 
     files: option "brazil" must be on documentclass
   . added visual enhancements on documentation files
   . changed the name of documentation files:
     from: "Manual de uso dos estilos bibliográficos do pacote abntex2cite: 
            estilos bibtex compatíveis com a ABNT NBR 6023"
       to: "O pacote abntex2cite: Estilos bibliográficos compatíveis com a ABNT NBR 6023"
     from: "Manual de uso do pacote abntex2cite: tópicos específicos da 
            ABNT NBR 10520:2002 e o estilo bibliográfico alfabético (sistema autor-data)"
       to: "O pacote abntex2cite: Tópicos específicos da ABNT NBR 10520:2002 e o 
            estilo bibliográfico alfabético (sistema autor-data)"
   . added information about bibliographies on examples.              
  
  2013/03/23 - v1.6
   . added support for typeset documents in different languages
   . enhancements in footnotes: 
     now there is a comma between sequential footnotes and 
     more spacing between index and text; 
   . added new example: glossary with abnTeX2
   . added xelatex, inputenc and fontenc information on abntex2.tex class manual;
   . added translations for section, subsection, subsubsection, paragraph and page in \autoref 
     in order to reach compliance to ABNT NBR 6024:2012
   . added information of compliance to ABNT NBR 6027:2012  
   . added translations to english of all macros from abnTeX2
   . added leaders to chapters in TOC 
   . changed implementation of \titulo, \autor, \data and
     \imprimirtitulo, \imprimirautor e \imprimirdata to be translations of
     \title, \author, \date, \thetitle, \theauthor e \thedate, respectively.
   . added how you can contribute to the abnTeX2 and minipage examples on abntex2-modelo-include.tex
   . complete fix iso-690-1987 option: year was placed for 
     twicebooklet, journalpart, manual, misc, unpublished, patent and unpublished on abntex2cite.sty
   . fix creation of macros \su@ExpandTwoArgs, \IfSubStringInString and \su@IfSubStringInString 
     imported from substr.sty on abntex2cite.sty
   . changed position of institutio's name at title page
   . removed unnecessary packages makeidx and hyperref from all examples; 
   . removed unnecessary package "lastpage" from:
     abntex2-modelo-projeto-pesquisa, abntex2-modelo-relatorio-tecnico and abntex2-modelo-artigo
   . added sections about internacionalization and about \autoref configurations on abntex2.tex class manual; 
   . added information about \and and \\ on description of macro \autor in abntex2.tex 
   . added enhancements to abntex2cite.tex and abntex2.tex about bibliographies
   . added examples of HEADERS and FOOTERS on abntex2-modelo-artigo.tex 
    
  2013/02/23 - v1.5
    abntex2.cls:
      . added \bookmarksetup{startatroot} in \textual and \postextual
      . added "siglas" and "simbolos" environments in order to 
        create "list of abbreviations and acronyms" and "list of symbols"
      . changed article headings to \pagestyle{plain}
      . removed \vspace*{1cm} on beginning of cover and titles pages
    abntex2-modelo-trabalho-academico.tex
      . removed \vspace*{1cm} on beginning of aprovation page
      . changed to use "siglas" and "simbolos" environments
      . minor changes
    abntex2-modelo-relatorio-tecnico.tex  
      . changed to use "siglas" and "simbolos" environments
      . minor changes
    abntex2-modelo-projeto-pesquisa.tex  
      . changed to use "siglas" and "simbolos" environments
      . minor changes
    abntex2-modelo-artigo.tex:
      . added simple spacing as a default option
      . minor changes
    abntex2-alf.bst and abntex2-num.bst:
      . fix iso-690-1987 option: year was placed twice
    abntex2cite.sty:
      . changed default style for author names in citations from small caps to upper case
      . added "versalete" option to use author names in small caps style on citations 
    abntex2cite-alf.tex:
      . added explanations about versalete option
      . added explanations about \authorcapstyle, \authorstyle and \yearstyle
    abntex2.tex:
      . added section about hyphenation
      . added ABNTEX NBR 6023 version 2002 compatibility information and information
      . added explanations about "siglas" and "simbolos" environments
        about the work in progress of updating manuals.
      . fix error about \partanexos* information (it was \partname*)
      . removed \vspace*{1cm} on beginning of cover and titles pages
    changed all models:
      . added hyphenation examples
      . added \frenchspacing as a default option to deal with space between phrases

  2013/02/04 - v1.4
    added \partanexos and \partapendices macros as a replacement to \appendixpage
    changed all models to use new  \partanexos and \partapendices macros
    bug fix on abntex2cite.sty: incorrect use of setspace
    general review of all examples
    updated abntex2-modelo-include-comandos:
     . added section about UTF-8
    updated abntex2.tex documentation:
     . added enumitem's reference in "Alíneas e subalíneas" section
     . added section about UTF-8
     . added sections about the main options of the class
     . added  \partanexos and \partapendices explanations
     . general review
    removed change logs from example files 
    changed README file structure
  
  2013/01/18 - v1.3
    added two new model: 
      . abntex2-modelo-relatorio-tecnico.tex: Technical report in compliance to ABNT NBR 10719:2011
      . abntex2-modelo-projeto-pesquisa.tex: Research project in compliance to ABNT NBR 15287:2011
    added on abntex.tex:
      . explanations about heading (not) created by \chapter* 
      . explanations about font and XeLaTeX
    added versions numbers in all files, documents and examples with a new build.sh script
    changed default font on examples and documentations to Latin Modern (lmodern)
    changed \pretextualchapter to change headings with the value of chapter title
    changed \ABNTEXchapterfont: now it uses a font style without serif (\sffamily)
    changed thesis model to add examples of \chapter*[heading title]{text title}
    changed title of the article model from "Modelo Canônico de Artigos Acadêmicos" 
      to "Modelo Canônico de Artigo Científico"
    changed title of the thesis model from "Modelo Canônico de Trabalhos Acadêmicos" 
      to "Modelo Canônico de Trabalho Acadêmico"
    changed title of abntex2 documentation from "A classe abntex2: Modelo canônico de
      trabalhos acadêmicos brasileiros compatível com as normas ABNT NBR 14724:2011,
      ABNT NBR 6024:2012 e outras" to "A classe abntex2: Documentos técnicos e científicos 
      brasileiros compatíveis com as normas ABNT"   
    as an example of \include, now all example documents share a single file 
      named abntex2-modelo-include-comandos.tex, that has the content from
      abntex2-modelo-trabalho-academico.tex and:
       . explanations about \include and \input macros
       . explanations about compiling LaTeX documents
    bug fix: singlespace on references produced by abntex2cite.sty
    bug fix: general orthographic errors

  2013/01/13 - v1.2.1
     added length \ABNTEXcitacaorecuo, useful on articles
     abntex2's twocolumn class option changes \ABNTEXcitacaorecuo to 1.8cm 
     changed \ABNTEXcitacaorecuo explanation on abntex2.tex and on examples 
     
  2013/01/12 - v1.2
     added article support to abntex2.cls
     added new article example
     changed canonical example: new commands, explanations and examples
     changed abntex2-modelo.tex file name to abntex2-modelo-trabalho-academico.tex 
     updated documentation 
     bug fixes on abntex2.cls
     added compatibility information to:
       . ABNT NBR 10719:2011: Informação e documentação - Relatório técnico e/ou científico - Apresentação
       . ABNT NBR 15287:2011: Informação e documentação - Projeto de pesquisa - Apresentação
       . ABNT NBR 6022-2003 - Informação e documentação - Artigo em publicação periódica científica impressa - Apresentação

  2013/01/05 - v1.1
     bug fixes on abnex2cite.sty when using with Beamer 
     changed \titulo, \autor and \data to do the same as \title, \author and \date  
      
  2012/12/20 - v1.0 
     initial release on CTAN 


INSTALLATION
-----------------------------------------------------------------

Are you new on TeX's world?
---------------------------

If you're new to this, see https://github.com/abntex/abntex2/wiki/Instalacao (portuguese)
or https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages (english) for more
information on installing packages.

"Automagic" instalation on a TeXLive system
-------------------------------------------

If you already have a TexLive system installed on a Unix-like system (Linux, Mac, BSD),
in order to install the abntex2 class and the abntex2cite package, uncompress the TDS file (something like 
abntex2-tds-VERSION.zip or abntex2-tds-VERSION.tar.gz) and type on a Terminal:

  make install

This will install abnTeX2 on your TeXLive system. 

Manual instalation
------------------

You can manually install the abntex2 class and the abntex2cite package in any LaTeX system (TeXLive, MiKTeX, 
among others) running over a Windows, Linux, Mac, BSD (among others) if you have:

  abntex2.cls	            The abntex2 class file.
  abntex2cite.sty	        The abntex2cite citation package file.
  abntex2abrev.sty	        Extension of abntex2cite package. It contains abbreviations helpers macros.
  abntex2-alf.bst	        Numeric citation style file.
  abntex2-num.bst			Alphanumeric (author-date) citation style file.
  abntex2-options.bib	    Default citation options configurations.
  
Put those files somewhere LaTeX can find them. Read the documentation of 
your LaTeX system to find out where this might be. 

Test the installation
---------------------

Type on a Terminal:

  texdoc abntex2
  
It should open the abntex2.pdf document file. You will find the current version of abnTeX2 on it.
 

DOCUMENTATION
-----------------------------------------------------------------

The abnTeX2 documentation consists of the following files:

  README								Instructions on installation and documentation.
  abntex2-modelo-trabalho-academico.tex	An usage example of abntex2 class and abntex2cite package producing a thesis
  abntex2-modelo-relatorio-tecnico.tex	An usage example of abntex2 class and abntex2cite package producing a technical report
  abntex2-modelo-projeto-pesquisa.tex	An usage example of abntex2 class and abntex2cite package producing a research project
  abntex2-modelo-artigo.tex				An usage example of abntex2 class and abntex2cite package producing an article
  abntex2-modelo-glossarios.tex			An usage example of abntex2 class and abntex2cite package producing a glossary
  abntex2-modelo-slides.tex				An usage example of a beamer presentation with abntex2cite package
  abntex2-modelo-include-comandos.tex	LaTeX examples shared by others files 
  abntex2-modelo-livro.tex				An usage example of abntex2 class and abntex2cite package producing a book
  abntex2-modelo-livro-bandeirinha.jpg		Image used by abntex2-modelo-livro.tex
  abntex2-modelo-livro-pintassilgo.jpg		Image used by abntex2-modelo-livro.tex
  abntex2-modelo-livro-saira-amarela.jpg	Image used by abntex2-modelo-livro.tex
  abntex2-modelo-img-grafico.pdf			Image used as an example
  abntex2-modelo-img-marca.pdf
  abntex2-modelo-references.bib			Bib references of examples above

  abntex2.tex							The main class documentation
  abntex2cite.tex						The abntex2cite package documentation
  abntex2cite-alf.tex					Additional alphanumeric (author-date) citation style documentation
  abntex2-doc.bib						Bib references used by documentation
  abntex2-doc-abnt-10520.bib			Specific ABNT NBR 10520:2001 and ABNT NBR 10520:2002 bib references entries
  abntex2-doc-abnt-6023.bib				Specific ABNT NBR 6023:2000 and ABNT NBR 6023:2002 bib references entries
  abntex2-doc-options.bib				Options configurations used by documentation
  abntex2-doc-test.bib					General bib references used by accordance tests

To produce any documentation above you also need:
  ltxdoc.cls   													(part of the standard LaTeX2e distribution)
  all installation files described in "INSTALLATION" section	(par of this bundle)

Compile the documentation as the example below. There are 3 PDF files of documentation and 4 of examples.
  
  pdflatex FILE.tex
  bibtex FILE.aux
  makeindex FILE
  latex2pdf FILE.tex
  latex2pdf FILE.tex
  
  (the "FILE" entry is one of the .tex file listed above)
  

COPYING AND MODIFICATION
-----------------------------------------------------------------

Copyright 2001-2003 abnTeX group at http://abntex.codigolivre.org.br
Copyright 2012-2018 abntex2 team at http://www.abntex.net.br

This package can be redistributed and/or modified under the terms
of the LaTeX Project Public License distributed from CTAN
archives in the directory macros/latex/base/lppl.txt; either
version 1.3 of the license, or (at your option) any later version.

Universities and other institutions are encouraged to customize 
front pages and others files and redistribute them to the users, 
but not to change the abnTeX2 files. You may customize almost all 
abnTeX2 commands with \renewcommand or using commands from memoir 
class. It is better than changing the files themselves.

HELP
-----------------------------------------------------------------

You can get help here:
 
www   http://www.abntex.net.br
group http://groups.google.com/group/abntex2

We need your help too. Access the project's home page and contact us.

Lauro César Araujo - laurocesar at laurocesar dot com


https://pt.overleaf.com/latex/templates/abntex-ufpr/bsswfjqykhhd
README: 
# ufpr-abntex2
==========================
O modelo criado:
 
 fig.jpg
 tipog.png
 figure.png são figuras e para compilar corretamente devem ser salvas na pasta fig/
 
 TermoA1.pdf
 FichaC1.pdf arquicos pdf do termo de aprovação  e ficha catalográfica. Para que os arquivos sejam inseridos nos 
 locais devidos, deve-se colocá-lo na pasta: metadados/ e retirar o algarismo 1 no final dos nomes dos arquivos.
 
 00-dados.tex 
   Possui os dados necessários para identificar o autor, instituição, trabalho, preambulo, resumo, epígrafe
   lista de siglas e de simbolos,....
 
 00-pacotes.tex 	
   Possui os pacotes customizados para o funcionamento de acordo com as normas da UFPR
   
 00-pretextual.tex 	
   Utilização dos arquivos de entrada de dados e de pacotes para criar os elementos prétextuais

 cap01.tex 	
   Demonstração do uso de comandos criados para a customização
   
 UFPR.sty 	 é o pacote de estilos
	
 main.tex 	 arquivo principal da customização, é o arquivo que deve ser compilado.
 
 referencias.bib exemplo de um arquivo de referências bibliográficas para exemplificar o uso do abntex2cite

 figure.png     arquivo da imagem de exemplo:  https://goo.gl/IpBzr1, deve ser colocada na pasta fig;
 FichaC1.pdf    arquivo da Ficha Catalográfica de exemplo: deve ser colocada na pasta metadados;
 TermoA1.pdf    arquivo do Termo de aprovação de exemplo: deve ser colocada na pasta metadados.

==========================
Instruções para o uso da customização:

1) Utilize a codificação UTF-8 para trabalhar com a customização;

2) Tenha a disposição um compilador com o pdfLaTeX;

3) Edite as informações solicitadas no arquivo 00.dados.tex

4) Compile o arquivo main.tex 

Qualquer dúvida ou comentário:  emilio.kavamura@ufpr.br ou eek.edu@outlook.com


Questões para resolver:

1 -  Eliminar referências do Rmardown e utilizaer somente a gerada pelo códifo Latex.
2 -  Alinhanhamento do Sumário
3 - Gerar arquvio Word de acordo com template
4 - Construir instruções específicas
5 - Adaptação para receber as classes memoir e ajustar problemas de normalização como página em branco, numeração, espaçamento. 



