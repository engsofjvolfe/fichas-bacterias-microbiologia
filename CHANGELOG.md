# Changelog

Todas as mudanças significativas deste projeto serão documentadas neste arquivo.

O formato é baseado no [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/), e este
projeto segue o [Versionamento Semântico](https://semver.org/lang/pt-BR/spec/v2.0.0.html).

## [Não publicado]

### Adicionado

- O texto de estudo de *Staphylococcus aureus*, nas sete etapas do manual de consistência.
- O texto de estudo de *Staphylococcus saprophyticus*, nas sete etapas do manual de
  consistência.
- O texto de estudo de *Staphylococcus epidermidis*, nas sete etapas do manual de
  consistência.
- O gancho do git que confere a forma do changelog antes de cada commit, com a peça da
  prateleira, e o texto dele no README, para ligá-lo numa cópia nova do repositório.
- A lista das divergências do livro, em `dados/divergencias.json`, e o cabeçalho do
  documento delas, que a peça da prateleira grava em `documentos-gerados/divergencias.md`.
- O link de cada versão no fim do changelog, com os modelos em
  `dados/confere-changelog-links.json`, que o gancho do git dá ao conferidor do changelog.

### Modificado

- A lista de nomes em itálico da configuração do conferidor de forma, com *S. lugdunensis*.
- No manual de consistência, a seção 4 passa a dizer que o texto é curto, mas com todas as
  informações necessárias, sem teto fixo de palavras.
- Os padrões proibidos do conferidor de forma saem da configuração dele: os deste projeto
  vão para `dados/confere-forma-proibidos.json`, e as marcas de IA vêm do arquivo comum da
  prateleira, dado no comando.
- No manual de consistência, o livro inteiro passa a ser a fonte: o porquê de um fato e a
  explicação de um termo podem vir de qualquer capítulo, citados no bloco de fonte da etapa;
  a explicação de um termo é a do livro, entre parênteses; o fato que o livro dá sem porquê
  fica sem ele; o texto não usa imagens; e a divergência do livro vai para o arquivo de
  divergências.
- No bloco de fonte, a citação de outro capítulo tem a própria linha de referência, sem o
  rótulo, que só a primeira citação do bloco leva: a configuração do conferidor de citações
  aceita a referência sem o rótulo, e os padrões proibidos das duas quebras do fim e do `&`
  valem também para ela.

## [0.2.0] - 2026-10-31

### Adicionado

- O texto de estudo de *Actinobacillus* (no livro, *Aggregatibacter actinomycetemcomitans*),
  nas sete etapas do manual de consistência.
- O texto de estudo de *Clostridium difficile*, nas sete etapas do manual de consistência.
- O texto de estudo de *Haemophilus influenzae*, nas sete etapas do manual de consistência.
- O texto de estudo de *Helicobacter pylori*, nas sete etapas do manual de consistência.
- O texto de estudo de *Neisseria meningitidis*, nas sete etapas do manual de consistência.
- O texto de estudo de *Proteus*, nas sete etapas do manual de consistência.
- O texto de estudo de *Pseudomonas aeruginosa*, nas sete etapas do manual de consistência.
- O texto de estudo de *Salmonella*, nas sete etapas do manual de consistência.
- O texto de estudo de *Shigella*, nas sete etapas do manual de consistência.

### Modificado

- A lista de nomes em itálico da configuração do conferidor de forma, com os nomes
  científicos novos dos textos e o termo latino *in vitro*.
- No manual de consistência, a seção 1 passa a apontar como modelos de forma e de tom os
  textos de *Clostridium difficile* e *Shigella*, e a seção 4 diz que o teto de tamanho do
  manual é menor que o do conferidor de forma.

### Corrigido

- Nos textos de *Clostridium tetani*, *Enterococcus* e *Neisseria gonorrhoeae*, o trecho do
  livro de uma etapa tinha uma supressão (`[...]`) num lugar em que nada fora omitido.

## [0.1.0] - 2026-10-29

### Adicionado

- Os textos de estudo de *Clostridium botulinum*, *Clostridium tetani*, *Enterococcus*,
  *Escherichia coli* e *Neisseria gonorrhoeae*, em sete etapas, cada uma terminando com o
  trecho do livro que a sustenta, copiado letra por letra, com o capítulo e a página.
- O manual de consistência, que diz como todo texto é escrito e formatado: o tom, a
  estrutura em sete etapas, a formatação e as regras de citação.
- A configuração dos dois conferidores (`dados/`): a forma de um texto de bactéria, com os
  nomes científicos que vão em itálico, e o bloco de fonte, conferido contra o capítulo
  citado.
- O README, com a regra das versões, este changelog e a lista do que falta.
- O `.gitignore`.

[Não publicado]: https://github.com/engsofjvolfe/fichas-nacterias-microbiologia/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/engsofjvolfe/fichas-nacterias-microbiologia/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/engsofjvolfe/fichas-nacterias-microbiologia/releases/tag/v0.1.0
