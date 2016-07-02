# myMdt

The important notice: please give me feedback. It means ALOT. and helps. everyone.


Versão atual: UFSM 2015

# estrutura
#### backbones
o documento é baseado na classe report. creio que com algumas modificações possa ser usado diretamente com outras classes, como article. não foi testado. modificações de estilo são realizadas a partir de pacotes.
novas listas para apendices e anexos foram geradas, porém suportam somente o nível principal. pretende-se implementar apendices e anexos com chapter, section, subsection, subsubsection em futuras versoes.
gráficos e outros elementos são gerados pelo pacote tgf/tikz
bibliografia é baseada no pacote biblatex com backend biber, impressa em 1 bloco ao final do conteudo textual

#### compilar
o template foi criado com o miktex e texstudio, sendo estes dois "recomendados". compilado com latex.

a ordem de compilacao utilizada é:

1. default compiler
2. default compiler
3. default bibliography
4. default compiler
5. default makeindex
6. default compiler

onde:
* default compiler = latex (configuracao padrao do texstudio)
* default bibliography = biber %
* default makeindex = makeindex %.nlo -s nomencl.ist -o %.nls

#### options
as opcoes de dupla face, lombada, coorientador, entre outros são implementados através de switches if.
os ifs podem ser habilitados ou desabilitados conforme necessidade no arquivo:

__txt/configuracoes.tex__

o arquivo apresenta comentários sucintos sobre a funcionalidade dos switches

# Summary of dirs
### images
diretório de imagens chamadas pelo texto

### pos
arquivos de elementos pos textuais, como referencias e indice

### pre
arquivos de elementos pré textuais, como capa, folha aprovação e sumário

### txt
arquivos de elementos "textuais", como dedicatória, capítulos e apêndices
~textuais: dedicatoria, abstract, resumo, e outros estão aqui
basicamente: todos os arquivos que o usuário deve inserir o texto

# Summary of files - os que fazem algo
### mymdt.sty
arquivo de estilo "mestre"

### mymdt.bbx, mymdt.cbx, mymdtstd.bbx
arquivos que são utilizados pelo biblatex para estilização de citacoes e lista de referencias. arquivos baseados, se não me engano, no estilo padrão alphabetic (ctrl c+ ctrl v + mods)

### mdt_template.ini, mdtRoot.txss
arquivos utilizados pelo Texstudio de configuracao. compatibilidade com outros computadores/sistemas/versoes/idk não testada.

### mdtRoot.tex
arquivo principal estrutural do trabalho.
aqui são incluidos itens como: capa, lombada, folha rosto, sumario, capitulos, etc.

# NOTAS DE USO
utilizar os seguintes comandos. alguns comandos são nativos dos pacotes, outros são mascarados/criados para aumento de funcionalidade.
## /index{CHAVE}
para incluir CHAVE no índice remissivo do documento

## /nomenclature{SIMBOLO}{SIGNIFICADO}
para incluir o SIGNIFICADO de SIMBOLO na lista de simbolos do documento

## /cite{XXX}
para incluir uma referência bibliográfica previamente definida

## /ref{XXX}
para incluir referência cruzada no texto

## /label{XXX}
para incluir uma âncora de referência cruzada

## /defSimb{xxx}{yyy}{nnn}
para definir um simbolo de chave xxx,
e forma curta yyy com forma extendida nnn

## /simb{xxx}
para adicionar um simbolo e entrada no indice

## /cite{xXyY}
para adicionar uma citação da bibliografia, definida em nnn.bib
para a adição de apendices de códigos fonte, lembrar de salvar o arquivo em UTF-8 sem BOM
