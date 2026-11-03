# TODO

O que falta fazer neste projeto, e só o que falta. O que fica pronto sai daqui e entra no
[CHANGELOG.md](CHANGELOG.md), na seção `Não publicado`.

## Os textos

1. Escrever as fichas de bactéria que ainda não têm arquivo, cada uma pelo manual de
   consistência, com os dois conferidores em zero erro.
2. Combinar a forma dos temas, das fichas de família e dos quadros, que ainda não têm
   modelo, antes de escrever o primeiro de cada.

## A conferência dos textos

3. Pedir à prateleira, no `confere-forma`, regras para a forma do tom, com os dados em
   `dados/confere-forma.json`: cada seção começa por um parágrafo, e não por lista,
   subtítulo ou citação; cada item de lista começa por um rótulo em negrito; cada sigla, na
   primeira vez em que aparece, tem a explicação entre parênteses logo depois dela, salvo as
   de uma lista das que dispensam explicação (como EUA e pH, e as que nenhum capítulo
   explica).
4. Conferir os textos antes de cada commit: um gancho do git que rode os dois conferidores
   nos textos que vão no commit e barre o commit quando algum der erro.
5. Corrigir os textos já escritos, a começar pelos cinco modelos, mexendo o mínimo e na voz
   de cada um, pelo que as regras do item 3 acusarem e pela revisão frase a frase, pelo tom
   e pelas regras de fonte do manual: etapas que abrem direto em lista ou subtítulo (na
   *Escherichia coli*, as etapas 5 a 7; na *Neisseria gonorrhoeae*, as 2, 3, 5, 6 e 7; no
   *Enterococcus*, as 2, 3 e 7), termos e siglas sem a explicação do livro entre parênteses,
   explicações, porquês e consequências que o livro não dá, passagens que divergem
   escolhidas ou juntadas no texto, imagens, nomes só para mostrar e fatos sem o porquê que
   o livro dá.

## Os documentos de apoio

6. Gravar pelas peças da prateleira (itens 6 a 10 do TODO dela) o glossário, as
   divergências, o dicionário das dúvidas e a lista dos apostos de IA, numa pasta própria,
   `documentos-de-apoio/`, fora de `documentos-gerados/`, que fica com as fichas: nenhum
   documento escrito à mão e nenhum JSON de `dados/` com texto corrido, só com os lugares no
   livro, as marcas e as escolhas. Por rebase, nos commits em que cada um desses documentos
   entrou no projeto e nos das fichas que puseram entradas nas listas, e não num commit
   novo; o texto das fichas fica como está.
7. Escrever no manual de consistência e nas instruções das sessões de trabalho a regra do
   aposto de IA: quando nenhum capítulo explica um termo, uma sigla ou um conceito de que o
   aluno precisa para seguir o texto, a explicação curta vem logo depois dele, entre `[IA: `
   e `]`, numa linha só. Ela pode trazer o fato geral que explica o termo, sem inventar
   (como o que é fagocitose), e nunca um fato da bactéria (número, epidemiologia,
   virulência, doença, diagnóstico, tratamento), um porquê ou uma consequência; não entra no
   bloco de fonte nem no glossário, e sai quando o livro der a explicação. A lista dos
   apostos sai das marcas (item 6).

## A publicação

8. Pôr a licença do projeto irmão (`recorte-microbiologia-bacteria`), a do conteúdo, CC
   BY-NC-SA 4.0, no `LICENSE-CONTENT.txt` copiado de lá, com os badges e a seção da licença
   no README; e o rodapé da licença no fim de cada documento, pela peça da prateleira do item
   11 do TODO dela. Depois do rodapé, o registro da conferência do baralho
   (`dados/baralho-anki-conferido.json`) se grava de novo, conferido que nos textos só o
   rodapé mudou.
9. Escrever o índice dos documentos, `INDICE.md`, na ordem de leitura, cada um com o que ele
   é, como o do projeto irmão.
