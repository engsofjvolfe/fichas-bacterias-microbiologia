# Recorte de Microbiologia: bactérias

Textos de estudo de microbiologia clínica, um por bactéria, escritos a partir dos capítulos
do livro *Microbiologia Médica*, de Murray. Cada texto responde, em linguagem didática, às
sete perguntas que o prefácio do livro propõe para estudar um microrganismo: qual é o
agente, onde vive e quem atinge, quando a infecção acontece, por que ele causa doença, o que
causa, como se confirma no laboratório e como se trata e se previne. Cada etapa termina com
o trecho do livro que a sustenta, copiado letra por letra, com o capítulo e a página.

## O que tem aqui

| Item | O que é |
| --- | --- |
| `documentos-gerados/` | os textos prontos; o `manual-de-consistencia.md`, que diz como todo texto é escrito e formatado: o tom, a estrutura em sete etapas, a formatação e as regras de citação; o `divergencias.md`, os fatos que o livro diz de formas diferentes, com a forma que os textos ensinam; o `glossario.md`, os termos que os textos explicam, com a explicação do livro; e o `dicionario-das-duvidas.md`, as dúvidas que o livro deixa, sob o lugar de cada uma |
| `baralhos-anki/` | o baralho do Anki da tabela dos patógenos, `bacterias.apkg`, com os cartões em `bacterias.csv`, e o manual de como os cartões se fazem e o baralho se refaz |
| `dados/` | a configuração das peças da prateleira que conferem os textos e fazem o baralho, as listas das divergências e do glossário, a forma dos códigos do dicionário das dúvidas e como rodar cada peça |
| `CHANGELOG.md` | o que mudou em cada versão |
| `TODO.md` | o que falta fazer |

## O que fica fora do repositório

- **As fontes** (`material-base/`): o livro, as normas da ABNT e as aulas. São obras de
  terceiros e não se publicam; os textos citam só trechos curtos, sempre com a fonte.
- **A prateleira de peças** (`prateleira/`): ferramentas que servem a qualquer projeto,
  num repositório próprio.
- **O controle dos textos** (`controle-dos-textos.md`): a lista dos textos a escrever, com o
  nome do arquivo de cada um.
- **As instruções das sessões de trabalho** (`.claude/`): ficam só na máquina em que os
  textos são escritos.
- **Os ganchos do git** (`.git/hooks/`): ficam em cada cópia do repositório; o do changelog
  está em [Antes de cada commit](#antes-de-cada-commit).

## Como os textos são conferidos

Antes de um texto ficar pronto, duas peças da prateleira o conferem, com a configuração
deste projeto, que está em [dados/](dados/README.md) junto com o comando de cada uma:

- **as citações:** cada trecho citado precisa estar, letra por letra, na transcrição do
  capítulo citado, e nas páginas citadas;
- **a forma:** o título e o subtítulo, os títulos das sete etapas, os divisores, o bloco de
  fonte no fim de cada etapa, os padrões proibidos (como caracteres invisíveis) e os nomes
  científicos em itálico.

O tom e o conteúdo, que nenhum conferidor confere, seguem o manual de consistência.

## Antes de cada commit

Um gancho do git confere a forma do `CHANGELOG.md` que vai no commit, o do índice, com a
peça [confere-changelog](prateleira/confere-changelog/README.md) da prateleira, a
configuração dela, que é a forma deste changelog, e os links de cada versão, de
`dados/confere-changelog-links.json`; com erro, o commit não se faz. Numa cópia nova do
repositório, ele se liga no arquivo `.git/hooks/pre-commit`, com permissão de rodar:

    #!/bin/sh
    # Antes de cada commit, confere a forma do CHANGELOG.md que vai no commit, o do indice, com a
    # peca confere-changelog da prateleira, que fica na pasta principal do repositorio (a que
    # guarda o .git), e com os links de cada versao da pasta do commit, quando ela os tem; vale
    # tambem no commit feito numa worktree.
    comum=$(cd "$(git rev-parse --git-common-dir)" && pwd) || exit 1
    topo=$(git rev-parse --show-toplevel) || exit 1
    peca="$(dirname "$comum")/prateleira/confere-changelog"
    links="$topo/dados/confere-changelog-links.json"
    set -- "$peca/configuracao.json" CHANGELOG.md --indice
    [ -f "$links" ] && set -- "$@" --links "$links"
    exec python3 -I "$peca/confere_changelog.py" "$@"

## As versões

As versões seguem o [Versionamento Semântico](https://semver.org/lang/pt-BR/spec/v2.0.0.html).
A parte pública do projeto são os textos: a forma que o manual de consistência dá a eles e o
nome do arquivo de cada um. Enquanto o primeiro número for 0, qualquer coisa pode mudar, e
cada publicação sobe o segundo número. Da 1.0.0 em diante, sobe:

- **o primeiro número** quando muda a forma de todos os textos ou o nome de um arquivo;
- **o segundo** quando entra um texto, ou algo que não muda a forma;
- **o terceiro** quando um texto é corrigido sem mudar a forma.
