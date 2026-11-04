# dados

Os dados deste projeto que as peças da prateleira usam. Aqui não há código: cada arquivo é
a configuração ou uma entrada de uma peça, e a peça roda direto da pasta `prateleira/`,
recebendo o arquivo daqui. O que é deste projeto fica só aqui; nada dele entra na
prateleira.

| Arquivo | Peça que o lê | O que diz |
| --- | --- | --- |
| `confere-citacoes.json` | [confere-citacoes](../prateleira/confere-citacoes/README.md) | como é o bloco "Fonte Exata no Livro" dos textos (a linha da referência, que só na primeira citação do bloco leva o rótulo, e a do trecho), que as fontes são os `chapterNN.md`, com páginas `## p. N` e blocos de imagem que não contam, e que a supressão é `[...]` |
| `confere-forma.json` | [confere-forma](../prateleira/confere-forma/README.md) | a forma de um texto de bactéria: as lacunas do título (o "do" ou "da" e o nome em itálico), o começo de cada etapa (um parágrafo, e não um item de lista, um subtítulo, uma citação, uma tabela ou um divisor), o divisor `---`, o bloco de fonte no fim de cada etapa, as siglas (o que é uma sigla e a forma da primeira vez, a da ABNT: entre parênteses, logo depois do nome completo), os nomes científicos que vão em itálico e o tamanho (850 a 2.100 palavras, que só dá aviso) |
| `confere-forma-esqueleto.md` | [confere-forma](../prateleira/confere-forma/README.md#o-esqueleto) | o esqueleto de um texto de bactéria: o título, com as lacunas, o subtítulo fixo e os 7 títulos das etapas |
| `confere-forma-proibidos.json` | [confere-forma](../prateleira/confere-forma/README.md#os-padrões-proibidos) | os padrões proibidos que são deste projeto: o título de nível 5, o subtítulo `####` numerado, a fórmula LaTeX, a palavra estrangeira, a grafia de Portugal, a supressão sem colchetes, a linha da fonte sem as duas quebras do fim, o `&` nas páginas da fonte, o comentário escondido e o item de lista sem o rótulo em negrito |
| `divergencias.json` | [divergencias](../prateleira/divergencias/README.md) | os fatos que o livro diz de formas diferentes, cada um com a forma que os textos ensinam e as outras, cada forma com o que diz e o trecho do livro que a dá |
| `divergencias-cabecalho.md` | [divergencias](../prateleira/divergencias/README.md) | o título e a abertura do documento das divergências, `documentos-gerados/divergencias.md` |
| `confere-changelog-links.json` | [confere-changelog](../prateleira/confere-changelog/README.md#os-links) | os modelos do link de cada versão no fim do changelog, que o gancho do git dá à peça |
| `confere-commit.json` | [confere-commit](../prateleira/confere-commit/README.md#a-configuração) | as conferências de cada commit, que o gancho do git roda sobre os arquivos do commit, como estão no índice: a forma do changelog, a forma e as citações dos textos de bactéria, as citações do glossário e das divergências e o rodapé dos documentos, cada uma com os padrões dos arquivos dela e o comando, com as peças e as fontes da pasta principal |
| `glossario.json` | [glossario](../prateleira/glossario/README.md) | os termos que os textos explicam, cada um com a explicação que o livro dá e o trecho do livro de onde ela vem |
| `glossario-cabecalho.md` | [glossario](../prateleira/glossario/README.md) | o título e a abertura do glossário, `documentos-gerados/glossario.md` |
| `dicionario-das-duvidas.json` | [dicionario-das-duvidas](../prateleira/dicionario-das-duvidas/README.md) | a forma dos códigos dos títulos do dicionário das dúvidas, `documentos-gerados/dicionario-das-duvidas.md`: o capítulo e a página do lugar de cada dúvida, como `19/210`, ou só o capítulo |
| `baralho-anki.json` | [baralho-anki](../prateleira/baralho-anki/README.md#a-configuração) | o baralho do Anki, `baralhos-anki/bacterias.apkg`: as colunas da tabela dos patógenos (o agente, a fonte e as cinco que viram cartão), as marcas de ênfase, o nome do baralho, o tipo de nota, com os campos, e a data da versão |
| `baralho-anki-frente.html`, `baralho-anki-verso.html` e `baralho-anki-estilo.css` | [baralho-anki](../prateleira/baralho-anki/README.md#como-rodar) | os modelos da frente e do verso do cartão do baralho e o estilo dele |
| `baralho-anki-conferido.json` | [baralho-anki](../prateleira/baralho-anki/README.md#o-registro-da-conferência) | o sha256 da tabela dos patógenos e de cada texto de estudo na última conferência de conteúdo dos cartões |
| `rodape.md` | [rodape](../prateleira/rodape/README.md#o-modelo) | o modelo do rodapé da licença, com o link para o `LICENSE-CONTENT.txt` a partir desta pasta, que vai no fim de cada documento; o confere-forma e o confere-changelog o deixam fora da conferência, e as divergências e o glossário o põem no fim do documento que gravam |
| `rodape.json` | [rodape](../prateleira/rodape/README.md#a-configuração) | os documentos que levam o rodapé, os `.md` do repositório, e os que ficam sem ele: os cabeçalhos dos documentos gravados, que entram no começo deles, e o esqueleto dos textos |

As marcas que uma ferramenta de IA deixa num texto (o caractere invisível ou o espaço
especial, e o resto de citação) servem a qualquer projeto e ficam na prateleira, no
`marcas-de-ia.json` do confere-forma, que o comando dá ao conferidor junto com os padrões
daqui.

## Como rodar

Da raiz do projeto, para um texto (ou vários):

    python3 -I prateleira/confere-citacoes/confere_citacoes.py dados/confere-citacoes.json material-base/gerados-ocr documentos-gerados/<texto>.md
    python3 -I prateleira/confere-forma/confere_forma.py dados/confere-forma.json dados/confere-forma-esqueleto.md documentos-gerados/<texto>.md --proibidos dados/confere-forma-proibidos.json --proibidos prateleira/confere-forma/marcas-de-ia.json --rodape dados/rodape.md

Os dois precisam sair com `0 erro(s)`. O que cada linha de `ERRO` quer dizer está no README
de cada peça.

O rodapé da licença não se escreve à mão: a peça do rodapé o põe no fim de cada documento
que ainda não o tem, o texto novo também, e confere, com `--conferir`, que todos o têm, o que
precisa sair com `0 sem o rodapé em dia`:

    python3 -I prateleira/rodape/rodape.py . dados/rodape.json dados/rodape.md
    python3 -I prateleira/rodape/rodape.py . dados/rodape.json dados/rodape.md --conferir

O documento das divergências, com o rótulo de cada forma, e o glossário se gravam da lista e
do cabeçalho de cada um, daqui, com o rodapé no fim, e as citações dos dois se conferem como
as de um texto:

    python3 -I prateleira/divergencias/divergencias.py dados/divergencias.json dados/divergencias-cabecalho.md documentos-gerados/divergencias.md --ensinada "**Forma ensinada:**" --outra "**Outra forma:**" --rodape dados/rodape.md
    python3 -I prateleira/glossario/glossario.py dados/glossario.json dados/glossario-cabecalho.md documentos-gerados/glossario.md --rodape dados/rodape.md
    python3 -I prateleira/confere-citacoes/confere_citacoes.py dados/confere-citacoes.json material-base/gerados-ocr documentos-gerados/divergencias.md documentos-gerados/glossario.md

Com `--conferir` no fim de cada comando que grava, nada se grava, e ele diz se o documento
está em dia. O dicionário das dúvidas se escreve à mão, e os códigos dos títulos dele se
conferem pela forma daqui:

    python3 -I prateleira/dicionario-das-duvidas/confere_dicionario.py dados/dicionario-das-duvidas.json documentos-gerados/dicionario-das-duvidas.md

O baralho do Anki se faz e se confere pelos comandos do [manual dele](../baralhos-anki/README.md#como-se-refaz).

Antes de cada commit, o gancho do git roda as conferências de `confere-commit.json` sobre os
arquivos do commit, como estão no índice (ver o [README](../README.md#antes-de-cada-commit));
o mesmo, sem fazer o commit, sobre o que está no índice agora:

    python3 -I prateleira/confere-commit/confere_commit.py dados/confere-commit.json

## Quando mudar

- A lista dos textos (`controle-dos-textos.md`) ganha ou perde uma bactéria: o nome dela,
  com o gênero e, na espécie, a abreviação, entra em `italico/nomes`, em
  `confere-forma.json`, ou sai de lá, se nenhum texto o usa.
- Um texto usa um nome científico que não está na lista: ele entra em `italico/nomes`, em
  `confere-forma.json`.
- O manual de consistência muda a forma dos textos: o mesmo muda aqui, no arquivo da peça que
  confere aquilo; o título, o subtítulo e os títulos das etapas, em
  `confere-forma-esqueleto.md`, e o resto da forma, como o bloco de fonte, nas configurações.
- Um padrão passa a ser proibido nos textos: entra em `confere-forma-proibidos.json` quando
  é deste projeto, e no `marcas-de-ia.json` da prateleira quando é uma marca que uma
  ferramenta de IA deixa em qualquer texto.
- O livro diz um fato de formas diferentes: a divergência entra em `divergencias.json`, com
  a forma que os textos ensinam e as outras, cada uma com a fonte na forma do bloco de fonte
  dos textos (a linha da referência, sem o rótulo, e a do trecho), e o documento das
  divergências se grava de novo.
- Um texto explica um termo com as palavras do livro: o termo entra em `glossario.json`, com
  a explicação e a fonte na forma do bloco de fonte dos textos, e o glossário se grava de
  novo.
- O livro deixa uma dúvida, como a transcrição truncada de uma página: ela entra no
  `documentos-gerados/dicionario-das-duvidas.md`, sob um título com os códigos do lugar
  (`capítulo/página`), e o conferidor do dicionário confere os títulos.
- A tabela dos patógenos ou um texto de estudo muda: o registro da conferência do baralho diz
  o que mudou, os cartões daquele agente se conferem de novo, e o baralho e o registro se
  gravam outra vez, pelo [manual do baralho](../baralhos-anki/README.md#como-se-refaz).
- Entra um arquivo `.md` que não é um documento inteiro, como o cabeçalho de um documento que
  uma peça grava: o padrão dele entra em `fora`, em `rodape.json`.
- Entra em `documentos-gerados/` um documento que não é texto de bactéria: ele entra em
  `fora`, em `confere-commit.json`, na conferência da forma dos textos e, se não tiver
  citações, na das citações.
- O aviso da licença muda: muda o `rodape.md`, a peça do rodapé grava de novo o fim de cada
  documento, e as divergências e o glossário se gravam de novo.

---

*Este documento está licenciado sob [CC BY-NC-SA 4.0](../LICENSE-CONTENT.txt).*
