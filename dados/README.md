# dados

Os dados deste projeto que as peças da prateleira usam. Aqui não há código: cada arquivo é
a configuração ou uma entrada de uma peça, e a peça roda direto da pasta `prateleira/`,
recebendo o arquivo daqui. O que é deste projeto fica só aqui; nada dele entra na
prateleira.

| Arquivo | Peça que o lê | O que diz |
| --- | --- | --- |
| `confere-citacoes.json` | [confere-citacoes](../prateleira/confere-citacoes/README.md) | como é o bloco "Fonte Exata no Livro" dos textos (a linha da referência, que só na primeira citação do bloco leva o rótulo, e a do trecho), que as fontes são os `chapterNN.md`, com páginas `## p. N` e blocos de imagem que não contam, e que a supressão é `[...]` |
| `confere-forma.json` | [confere-forma](../prateleira/confere-forma/README.md) | a forma de um texto de bactéria: o título e o subtítulo fixos, os 7 títulos das etapas, o divisor `---`, o bloco de fonte no fim de cada etapa, os nomes científicos que vão em itálico e o tamanho (850 a 2.100 palavras, que só dá aviso) |
| `confere-forma-proibidos.json` | [confere-forma](../prateleira/confere-forma/README.md#os-padrões-proibidos) | os padrões proibidos que são deste projeto: o título de nível 5, o subtítulo `####` numerado, a fórmula LaTeX, a palavra estrangeira, a grafia de Portugal, a supressão sem colchetes, a linha da fonte sem as duas quebras do fim, o `&` nas páginas da fonte e o comentário escondido |
| `divergencias.json` | [divergencias](../prateleira/divergencias/README.md) | os fatos que o livro diz de formas diferentes, cada um com a forma que os textos ensinam e as outras, cada forma com o que diz e o trecho do livro que a dá |
| `divergencias-cabecalho.md` | [divergencias](../prateleira/divergencias/README.md) | o título e a abertura do documento das divergências, `documentos-gerados/divergencias.md` |
| `confere-changelog-links.json` | [confere-changelog](../prateleira/confere-changelog/README.md#os-links) | os modelos do link de cada versão no fim do changelog, que o gancho do git dá à peça |

As marcas que uma ferramenta de IA deixa num texto (o caractere invisível ou o espaço
especial, e o resto de citação) servem a qualquer projeto e ficam na prateleira, no
`marcas-de-ia.json` do confere-forma, que o comando dá ao conferidor junto com os padrões
daqui.

## Como rodar

Da raiz do projeto, para um texto (ou vários):

    python3 -I prateleira/confere-citacoes/confere_citacoes.py dados/confere-citacoes.json material-base/gerados-ocr documentos-gerados/<texto>.md
    python3 -I prateleira/confere-forma/confere_forma.py dados/confere-forma.json documentos-gerados/<texto>.md --proibidos dados/confere-forma-proibidos.json --proibidos prateleira/confere-forma/marcas-de-ia.json

Os dois precisam sair com `0 erro(s)`. O que cada linha de `ERRO` quer dizer está no README
de cada peça.

O documento das divergências se grava da lista e do cabeçalho daqui, com o rótulo de cada
forma, e as citações dele se conferem como as de um texto:

    python3 -I prateleira/divergencias/divergencias.py dados/divergencias.json dados/divergencias-cabecalho.md documentos-gerados/divergencias.md --ensinada "**Forma ensinada:**" --outra "**Outra forma:**"
    python3 -I prateleira/confere-citacoes/confere_citacoes.py dados/confere-citacoes.json material-base/gerados-ocr documentos-gerados/divergencias.md

Com `--conferir` no fim do primeiro, nada se grava, e ele diz se o documento está em dia.

## Quando mudar

- A lista dos textos (`controle-dos-textos.md`) ganha ou perde uma bactéria: o nome dela,
  com o gênero e, na espécie, a abreviação, entra em `italico/nomes`, em
  `confere-forma.json`, ou sai de lá, se nenhum texto o usa.
- Um texto usa um nome científico que não está na lista: ele entra em `italico/nomes`, em
  `confere-forma.json`.
- O manual de consistência muda a forma dos textos (títulos, subtítulo, bloco de fonte): o
  mesmo muda aqui, no arquivo da peça que confere aquilo.
- Um padrão passa a ser proibido nos textos: entra em `confere-forma-proibidos.json` quando
  é deste projeto, e no `marcas-de-ia.json` da prateleira quando é uma marca que uma
  ferramenta de IA deixa em qualquer texto.
- O livro diz um fato de formas diferentes: a divergência entra em `divergencias.json`, com
  a forma que os textos ensinam e as outras, cada uma com a fonte na forma do bloco de fonte
  dos textos (a linha da referência, sem o rótulo, e a do trecho), e o documento das
  divergências se grava de novo.
