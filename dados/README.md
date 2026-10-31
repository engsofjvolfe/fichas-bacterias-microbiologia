# dados

Os dados deste projeto que as peças da prateleira usam. Aqui não há código: cada arquivo é
a configuração de uma peça, e a peça roda direto da pasta `prateleira/`, recebendo o arquivo
daqui. O que é deste projeto fica só aqui; nada dele entra na prateleira.

| Arquivo | Peça que o lê | O que diz |
| --- | --- | --- |
| `confere-citacoes.json` | [confere-citacoes](../prateleira/confere-citacoes/README.md) | como é o bloco "Fonte Exata no Livro" dos textos (a linha da referência, que só na primeira citação do bloco leva o rótulo, e a do trecho), que as fontes são os `chapterNN.md`, com páginas `## p. N` e blocos de imagem que não contam, e que a supressão é `[...]` |
| `confere-forma.json` | [confere-forma](../prateleira/confere-forma/README.md) | a forma de um texto de bactéria: o título e o subtítulo fixos, os 7 títulos das etapas, o divisor `---`, o bloco de fonte no fim de cada etapa, os nomes científicos que vão em itálico e o tamanho (850 a 2.100 palavras, que só dá aviso) |
| `confere-forma-proibidos.json` | [confere-forma](../prateleira/confere-forma/README.md#os-padrões-proibidos) | os padrões proibidos que são deste projeto: o título de nível 5, o subtítulo `####` numerado, a fórmula LaTeX, a palavra estrangeira, a grafia de Portugal, a supressão sem colchetes, a linha da fonte sem as duas quebras do fim, o `&` nas páginas da fonte e o comentário escondido |

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
