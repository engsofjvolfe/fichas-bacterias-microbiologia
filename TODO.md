# TODO

O que falta fazer neste projeto, e só o que falta. O que fica pronto sai daqui e entra no
[CHANGELOG.md](CHANGELOG.md), na seção `Não publicado`.

## O repositório

1. Quando houver um repositório remoto, pôr no fim do changelog o link de cada versão.

## Os textos

2. Escrever as fichas de bactéria que ainda não têm arquivo, cada uma pelo manual de
   consistência, com os dois conferidores em zero erro.
3. Combinar a forma dos temas, das fichas de família e dos quadros, que ainda não têm
   modelo, antes de escrever o primeiro de cada.
4. Usar no projeto o glossário e o dicionário das dúvidas, da prateleira, com os dados em
   `dados/`, como as divergências; antes, combinar o que entra no glossário e como os textos
   se ligam a ele, e a forma dos códigos do dicionário, como o capítulo e a página do lugar
   de cada dúvida.

## A conferência dos textos

5. Pedir à prateleira, no `confere-forma`, regras para a forma do tom, com os dados em
   `dados/confere-forma.json`: cada seção começa por um parágrafo, e não por lista,
   subtítulo ou citação; cada item de lista começa por um rótulo em negrito; cada sigla, na
   primeira vez em que aparece, tem a explicação entre parênteses logo depois dela, salvo as
   de uma lista das que dispensam explicação (como EUA e pH, e as que nenhum capítulo
   explica).
6. Conferir os textos antes de cada commit: um gancho do git que rode os dois conferidores
   nos textos que vão no commit e barre o commit quando algum der erro.
7. Corrigir os textos já escritos, a começar pelos cinco modelos, mexendo o mínimo e na voz
   de cada um, pelo que as regras do item 5 acusarem e pela revisão frase a frase, pelo tom
   e pelas regras de fonte do manual: etapas que abrem direto em lista ou subtítulo (na
   *Escherichia coli*, as etapas 5 a 7; na *Neisseria gonorrhoeae*, as 2, 3, 5, 6 e 7; no
   *Enterococcus*, as 2, 3 e 7), termos e siglas sem a explicação do livro entre parênteses,
   explicações, porquês e consequências que o livro não dá, passagens que divergem
   escolhidas ou juntadas no texto, imagens, nomes só para mostrar e fatos sem o porquê que
   o livro dá.
