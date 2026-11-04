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
- O glossário dos termos que os textos explicam, com a lista em `dados/glossario.json` e o
  cabeçalho, que a peça da prateleira grava em `documentos-gerados/glossario.md`.
- O dicionário das dúvidas que o livro deixa, `documentos-gerados/dicionario-das-duvidas.md`,
  cada uma sob os códigos do lugar (o capítulo e a página), com a forma dos códigos em
  `dados/dicionario-das-duvidas.json`, que a peça da prateleira confere.
- O texto de estudo de *Streptococcus agalactiae*, nas sete etapas do manual de
  consistência.
- Na lista das divergências, os quatro fatos do texto de *Streptococcus agalactiae* que o
  livro diz de formas diferentes: os locais de colonização, as condições que aumentam o
  risco fora da gravidez, as infecções mais comuns em homens e mulheres não grávidas e o uso
  dos testes de antígeno.
- No glossário, os termos que o texto de *Streptococcus agalactiae* explica.
- No dicionário das dúvidas, duas do capítulo 19: o início da doença neonatal precoce no
  Boxe 19.1 e a unidade da taxa da doença neonatal.
- O texto de estudo de *Enterobacter*, nas sete etapas do manual de consistência.
- No glossário, os termos que o texto de *Enterobacter* explica.
- No dicionário das dúvidas, uma do capítulo 25: o número do *Enterobacter* na Figura 25.3,
  truncado na transcrição.
- O texto de estudo de *Streptococcus pneumoniae*, nas sete etapas do manual de
  consistência.
- Na lista das divergências, os três fatos do texto de *Streptococcus pneumoniae* que o
  livro diz de formas diferentes: a sensibilidade da cultura, a do teste de antígeno na
  urina e a quem se recomenda a vacina polissacarídica.
- No glossário, os termos que o texto de *Streptococcus pneumoniae* explica.
- O texto de estudo de *Streptococcus pyogenes*, nas sete etapas do manual de consistência.
- No glossário, os termos que o texto de *Streptococcus pyogenes* explica.
- O texto de estudo de *Mycobacterium tuberculosis*, nas sete etapas do manual de
  consistência.
- Na lista das divergências, os três fatos do texto de *Mycobacterium tuberculosis* que o
  livro diz de formas diferentes: quem tem maior risco de doença, a sensibilidade da
  microscopia e os métodos mais usados na identificação.
- No glossário, os termos que o texto de *Mycobacterium tuberculosis* explica.
- No dicionário das dúvidas, duas dos capítulos 12, 14 e 22: a cobertura "antifagocítica" das
  micobactérias e a profilaxia com "pirazinamida e etambutol ou levofloxacino".
- O texto de estudo de *Vibrio*, nas sete etapas do manual de consistência.
- Na lista das divergências, o fato do texto de *Vibrio* que o livro diz de formas
  diferentes: o uso dos imunoensaios de antígeno no diagnóstico das infecções por
  *Vibrio cholerae*.
- No glossário, os termos que o texto de *Vibrio* explica.
- No dicionário das dúvidas, uma do capítulo 26: a medida dos bacilos de *Vibrio*, com três
  números ligados pela mesma palavra.
- O texto de estudo de *Yersinia enterocolitica*, nas sete etapas do manual de
  consistência.
- No glossário, os termos que o texto de *Yersinia enterocolitica* explica.
- A tabela dos patógenos em palavras-chave, `documentos-gerados/tabela.md`: a doença típica,
  onde vive, quem adoece, os fatores de virulência e o tratamento de cada agente, com o
  texto de estudo de onde saíram.
- O baralho do Anki da tabela dos patógenos, em `baralhos-anki/`: os 120 cartões, cinco por
  agente, cada um com a pergunta, a resposta, escrita pelo texto de estudo, e o trecho do
  texto que a sustenta, o pacote e o manual de como os cartões se fazem e o baralho se refaz
  pela peça `baralho-anki` da prateleira; a configuração, os modelos do cartão e o registro
  da conferência de conteúdo, em `dados/`.
- A licença do conteúdo, a CC BY-NC-SA 4.0, no `LICENSE-CONTENT.txt`, com o badge e a seção
  da licença no README.
- O rodapé da licença no fim de cada documento, que a peça `rodape` da prateleira põe e
  confere, com o modelo em `dados/rodape.md` e, em `dados/rodape.json`, os documentos que
  ficam sem ele, os cabeçalhos dos documentos gravados.
- Na conferência da forma dos textos, as regras do tom: cada etapa começa por um parágrafo,
  e não por um item de lista, um subtítulo, uma citação, uma tabela ou um divisor; cada item
  de lista começa por um rótulo em negrito; e cada sigla, na primeira vez em que aparece,
  vem entre parênteses, logo depois do nome completo, como manda a ABNT NBR 14724.
- A conferência de cada commit pela peça `confere-commit` da prateleira, com as conferências
  em `dados/confere-commit.json`, sobre os arquivos do commit como estão no índice: a forma e
  as citações dos textos que vão no commit, as citações do glossário e das divergências, o
  rodapé dos documentos e a forma do changelog; com erro, o commit não se faz.
- Na lista das divergências, os dois fatos do texto de *Clostridium difficile* que o livro diz
  de formas diferentes: o que faz cada uma das duas toxinas na parede do intestino e o que
  cresce em excesso no intestino do paciente exposto a antibacterianos.
- No glossário, os termos que o texto de *Clostridium difficile* explica.
- A escrita nas listas das divergências e do glossário e no CSV do baralho pela peça
  `listas-e-tabelas` da prateleira, com a configuração em `dados/listas-e-tabelas.json` e o
  modelo da citação da fonte, que monta cada citação do capítulo, das páginas e do trecho; os
  arquivos do modelo ficam sem o rodapé da licença, e o comando está em `dados/README.md`.
- A regra do aposto de IA, no manual de consistência: o termo, a sigla ou o conceito que
  nenhum capítulo explica, e de que o aluno precisa para seguir o texto, ganha a explicação
  curta entre `[IA: ` e `]`, numa linha só: o fato geral que o explica, nunca um fato da
  bactéria, fora do bloco de fonte e do glossário; na sigla, o aposto é o nome completo,
  antes dela. Na conferência da forma, a abertura do aposto não se lê como sigla.

### Modificado

- A lista de nomes em itálico da configuração do conferidor de forma, com *S. lugdunensis*,
  *Enterobacter cloacae*, *Citrobacter*, *Morganella*, *M. bovis*, *Vibrio cholerae*,
  *Vibrio parahaemolyticus*, *Vibrio vulnificus*, *Y. pestis*, *Y. pseudotuberculosis* e o
  termo latino *tuberculum*.
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
- No baralho do Anki, as respostas dos cartões passam a ser curtas, em frases completas,
  ligadas a cada parte da pergunta, com o termo técnico explicado nas palavras do texto de
  estudo; o pacote sai de novo, com a data da versão nova.
- No manual de consistência, o texto termina no rodapé da licença, que começa por um divisor.
- O documento das divergências e o glossário se gravam com o rodapé da licença no fim, e o
  conferidor de forma e o gancho do git do changelog o deixam fora da conferência: os
  comandos de `dados/README.md` e o texto do gancho, no README, ganham o modelo do rodapé.
- O registro da conferência do baralho, gravado de novo com o rodapé nos textos de estudo e
  na tabela, em que só ele mudou.
- O título, o subtítulo e os títulos das etapas saem da configuração do conferidor de forma e
  vão para o esqueleto dos textos, `dados/confere-forma-esqueleto.md`, que o comando dá ao
  conferidor; o "do" ou "da" e o nome do título são lacunas, e a configuração passa à versão
  2, só com a forma.
- No manual de consistência, na regra 4 e na checklist, a sigla, na primeira vez em que
  aparece, vem entre parênteses, logo depois do nome completo que o livro dá, como manda a
  ABNT NBR 14724.
- O gancho do git antes de cada commit passa a rodar a peça `confere-commit`, que confere
  também o changelog; o texto dele, no README, muda, e cada cópia do repositório o liga de
  novo.

### Corrigido

- O texto de estudo de *Clostridium difficile*, pelo manual de consistência: cada termo com a
  explicação que o livro dá, a primeira vez da PCR na forma da ABNT, os rótulos e as
  explicações sem imagem, só os porquês e as consequências que o livro dá e, nas toxinas e no
  crescimento excessivo, a forma que a lista das divergências ensina.
- No baralho do Anki, os cartões de *Clostridium difficile* da doença típica, de quem adoece e
  do fator de virulência, pelo texto corrigido; o pacote sai de novo, com a data da versão
  nova, e o registro da conferência se grava de novo.

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

---

*Este documento está licenciado sob [CC BY-NC-SA 4.0](LICENSE-CONTENT.txt).*
