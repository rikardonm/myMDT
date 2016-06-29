# myMdt

Versão atual: UFSM 2015



# NOTAS DE USO

## utilizar abaixo para compilar o indice e bibliografia

makeindex %.nlo -s nomencl.ist -o %.nls
biber %

## modificar as flags somente no arquivo configuracoes

# utilizar

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
e forma curta yyy com forma extendida yyy

## /simb{xxx}
para adicionar um simbolo e entrada no indice

## /cite{xXyY}
para adicionar uma citação da bibliografia, definida em nnn.bib
para a adição de apendices de códigos fonte, lembrar de salvar o arquivo em UTF-8 sem BOM
