# TODO

O que falta fazer neste projeto, e só o que falta. O que fica pronto sai daqui e entra no
[CHANGELOG.md](CHANGELOG.md), na seção `Não publicado`.

## O repositório

1. Quando houver um repositório remoto, pôr no fim do changelog o link de cada versão.

## Os ganchos

2. Ligar o gancho do changelog, quando a prateleira o tiver (ver o TODO dela).

## Os textos

3. Escrever as fichas de bactéria que ainda não têm arquivo, cada uma pelo manual de
   consistência, com os dois conferidores em zero erro.
4. Combinar a forma dos temas, das fichas de família e dos quadros, que ainda não têm
   modelo, antes de escrever o primeiro de cada.

## A conferência dos textos

5. Tornar exata a regra 4 do manual de consistência, para ela poder ser conferida: dizer se
   a tradução de um termo vai só entre parênteses ou se vale também logo depois dele,
   separada por vírgula, como em vários textos ("no começo do duodeno, a primeira porção do
   intestino"), e se ela pode dar o sentido comum da palavra quando o capítulo não o dá.
6. Pedir à prateleira, no `confere-forma`, regras para a forma do tom, com os dados em
   `dados/confere-forma.json`: cada seção começa por um parágrafo, e não por lista,
   subtítulo ou citação; cada item de lista começa por um rótulo em negrito; cada sigla, na
   primeira vez em que aparece, tem a explicação ao lado, salvo as de uma lista das que
   dispensam explicação (como EUA e pH).
7. Conferir os textos antes de cada commit: um gancho do git que rode os dois conferidores
   nos textos que vão no commit e barre o commit quando algum der erro.
8. Corrigir os textos já escritos, a começar pelos cinco modelos, mexendo o mínimo e na voz
   de cada um, pelo que as regras do item 6 acusarem e pela revisão do tom frase a frase:
   etapas que abrem direto em lista ou subtítulo (na *Escherichia coli*, as etapas 5 a 7; na
   *Neisseria gonorrhoeae*, as 2, 3, 5, 6 e 7; no *Enterococcus*, as 2, 3 e 7), termos e
   siglas sem tradução, nomes só para mostrar e fatos sem o porquê.
