# Recorte de Microbiologia: bactérias

![Licenca conteudo](https://img.shields.io/badge/Conte%C3%BAdo-CC_BY--NC--SA_4.0-blue)

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
| `dados/` | a configuração das peças da prateleira que conferem os textos, põem o rodapé da licença, fazem o baralho e escrevem nas listas e no baralho, as listas das divergências e do glossário, a forma dos códigos do dicionário das dúvidas, os modelos do rodapé e da citação e como rodar cada peça |
| `CHANGELOG.md` | o que mudou em cada versão |
| `TODO.md` | o que falta fazer |
| `LICENSE-CONTENT.txt` | a licença do conteúdo, a CC BY-NC-SA 4.0 (ver [Licença](#licença)) |

## O que fica fora do repositório

- **As fontes** (`material-base/`): o livro, as normas da ABNT e as aulas. São obras de
  terceiros e não se publicam; os textos citam só trechos curtos, sempre com a fonte.
- **A prateleira de peças** (`prateleira/`): ferramentas que servem a qualquer projeto,
  num repositório próprio.
- **O controle dos textos** (`controle-dos-textos.md`): a lista dos textos a escrever, com o
  nome do arquivo de cada um.
- **As instruções das sessões de trabalho** (`.claude/`): ficam só na máquina em que os
  textos são escritos.
- **Os ganchos do git** (`.git/hooks/`): ficam em cada cópia do repositório; o que confere
  cada commit está em [Antes de cada commit](#antes-de-cada-commit).

## Como os textos são conferidos

Antes de um texto ficar pronto, duas peças da prateleira o conferem, com a configuração
deste projeto, que está em [dados/](dados/README.md) junto com o comando de cada uma:

- **as citações:** cada trecho citado precisa estar, letra por letra, na transcrição do
  capítulo citado, e nas páginas citadas;
- **a forma:** o título e o subtítulo, os títulos das sete etapas, os divisores, o começo de
  cada etapa, que é um parágrafo, o rótulo em negrito no começo de cada item de lista, a
  primeira vez de cada sigla, entre parênteses, logo depois do nome completo, como manda a
  ABNT, o bloco de fonte no fim de cada etapa, os padrões proibidos (como caracteres
  invisíveis) e os nomes científicos em itálico.

O resto do tom e o conteúdo, que nenhum conferidor confere, seguem o manual de consistência.
O rodapé da licença, no fim de cada documento, se põe e se confere pela peça
[rodape](prateleira/rodape/README.md), com o modelo e os documentos que ficam sem ele em
`dados/`.

## Antes de cada commit

Um gancho do git confere cada commit com a peça
[confere-commit](prateleira/confere-commit/README.md) da prateleira, que roda as conferências
de `dados/confere-commit.json` sobre os arquivos do commit, como estão no índice: a forma do
changelog, com os links de cada versão e o modelo do rodapé; a forma e as citações dos textos
que vão no commit, e as do glossário e das divergências; e o rodapé de todos os documentos,
quando o commit muda algum. As peças e as fontes vêm da pasta principal do repositório, a que
guarda o `.git`, também no commit feito numa worktree. Com erro, o commit não se faz. Numa
cópia nova do repositório, o gancho se liga no arquivo `.git/hooks/pre-commit`, com permissão
de rodar:

    #!/bin/sh
    # Antes de cada commit, roda as conferencias de dados/confere-commit.json, da pasta do commit,
    # sobre os arquivos do commit, como estao no indice, com a peca confere-commit da prateleira,
    # que fica na pasta principal do repositorio (a que guarda o .git); vale tambem no commit
    # feito numa worktree.
    comum=$(cd "$(git rev-parse --git-common-dir)" && pwd) || exit 1
    topo=$(git rev-parse --show-toplevel) || exit 1
    exec python3 -I "$(dirname "$comum")/prateleira/confere-commit/confere_commit.py" "$topo/dados/confere-commit.json"

## As versões

As versões seguem o [Versionamento Semântico](https://semver.org/lang/pt-BR/spec/v2.0.0.html).
A parte pública do projeto são os textos: a forma que o manual de consistência dá a eles e o
nome do arquivo de cada um. Enquanto o primeiro número for 0, qualquer coisa pode mudar, e
cada publicação sobe o segundo número. Da 1.0.0 em diante, sobe:

- **o primeiro número** quando muda a forma de todos os textos ou o nome de um arquivo;
- **o segundo** quando entra um texto, ou algo que não muda a forma;
- **o terceiro** quando um texto é corrigido sem mudar a forma.

## Licença

Uma licença diz o que cada pessoa pode fazer com um trabalho: usar, mudar, repassar. O
conteúdo deste projeto usa uma, e o material de outras pessoas fica fora dela:

| Parte | Licença | Significa que... |
| --- | --- | --- |
| Conteúdo (tudo o que não é material de outras pessoas: os textos, o manual, as listas, a tabela, o baralho, as configurações e os dados) | [CC BY-NC-SA 4.0](LICENSE-CONTENT.txt) | Pode usar e adaptar dando o crédito, sem fins comerciais, mantendo a mesma licença |
| Os trechos do livro que os documentos citam, como o bloco de fonte de cada etapa | Nenhuma: são do livro | Vão só como citação, curtos e sempre com a fonte |
| As fontes, fora do repositório (ver [O que fica fora do repositório](#o-que-fica-fora-do-repositório)) | Nenhuma: não são deste projeto | Não se publicam nem se repassam |

A divisão vale por tipo de arquivo, não por uma lista fechada: um arquivo novo do mesmo tipo
já nasce coberto. Cada documento termina no aviso da licença, que a peça
[rodape](prateleira/rodape/README.md) da prateleira põe e confere, com o modelo em
`dados/rodape.md`. As peças da prateleira, que conferem os textos e fazem o baralho, ficam no
repositório dela, com as licenças dele.

Ao reusar o conteúdo, o crédito é: "Recorte de Microbiologia: bactérias, licenciado sob CC
BY-NC-SA 4.0", com o link para este projeto.

---

*Este documento está licenciado sob [CC BY-NC-SA 4.0](LICENSE-CONTENT.txt).*
