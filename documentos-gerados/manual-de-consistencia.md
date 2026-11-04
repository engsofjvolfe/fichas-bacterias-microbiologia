# Manual de Consistência para Produção de Textos de Microbiologia (Versão Atualizada)

## 1. Objetivo e Princípios Fundamentais

Este manual estabelece o padrão único para a criação, formatação e organização dos textos de estudo em microbiologia clínica: um texto por bactéria, escrito a partir do livro, o Murray, de que os capítulos 12 a 35 estão transcritos em `material-base/gerados-ocr/chapterNN.md`: o capítulo que trata da bactéria e, para o porquê de um fato e a explicação de um termo, qualquer outro desses capítulos, lido inteiro. O objetivo é garantir que todos os documentos mantenham rigor científico, clareza pedagógica narrativa e padronização visual completa.

Os textos de *Clostridium difficile* e *Shigella* são os modelos de forma e de tom: na dúvida, faça como eles. Onde um texto já escrito e uma regra deste manual divergem, vale a regra.

## 2. Princípios Pedagógicos e de Linguagem

O texto ensina quem está aprendendo. Ele não fica repetindo o livro, não é denso nem grande, tem início, meio e fim, não deixa de fora o que precisa aparecer e não traz informação que não serve para nada. Também não usa nomes nem rotas bioquímicas só para mostrar a quem já sabe.

- **Proibição do "Dump" de Dados Expositivo:** É estritamente proibido listar toxinas, enzimas ou exames em formatos de catálogos secos. O texto deve obrigatoriamente explicar o mecanismo e a lógica biológica/clínica que o livro dá para cada elemento.
- **Glossário Contextual Integrado:** Cada sigla (ex.: SARM, MRSA, SASM, TSST-1, PCR) e cada termo molecular especializado (ex.: desmogleína-1, PBP2a, gene mecA) vêm, no exato momento da primeira menção, com o significado e a relação com a doença que o livro dá (seção 3, regra 4).
- **Equilíbrio entre Rigor Acadêmico e Acessibilidade Didática:** O tom é formal e correto, sem gírias nem infantilizações, mas construído como explicação, em encadeamento de causa e efeito. Português do Brasil, sem palavras estrangeiras soltas; termos latinos consagrados vão em itálico.

## 3. O Padrão do Tom

Todo trecho escrito ou corrigido segue o jeito de escrever dos modelos:

1. **A etapa abre com a lógica.** Uma frase de entrada dá a ideia central e anuncia o que vem, muitas vezes por contraste: "O *C. difficile* pode viver no intestino sem causar doença. Quem adoece é quem toma antibióticos, em geral depois de passar por um serviço de saúde:".
2. **Rótulo em negrito, depois a explicação.** Cada item começa por um rótulo que diz o papel da coisa ("**Via fecal-oral, de pessoa para pessoa:**", "**Suspensão do Antibiótico Envolvido:**", "**Alerta de Bancada:**") e segue com a explicação.
3. **O porquê e a consequência vêm do livro.** Cada fato vem com o porquê ou com a consequência que o livro dá para ele: "exige meios seletivos, porque a microbiota normal, abundante, pode esconder o patógeno"; "de modo que ter o plasmídio não garante que ele funcione"; "Isso ocorre porque"; "resultando em". O fato que o livro dá sem porquê fica sem porquê (seção 7).
4. **Cada termo vem com a explicação do livro, entre parênteses.** Todo termo técnico, na primeira vez em que aparece, vem com a explicação que o livro dá, com as palavras dele, entre parênteses, logo depois dele: "**apoptose** (morte celular programada)", "**tenesmo** (esforço para defecar)". A sigla, na primeira vez em que aparece, vem entre parênteses, logo depois do nome completo que o livro dá, como manda a ABNT NBR 14724 (5.6): "*E. coli* enteroinvasiva (EIEC)". A explicação pode vir de qualquer capítulo, lido inteiro, e o trecho que a dá entra no bloco de fonte da etapa (seção 6). O termo, a sigla ou o conceito que nenhum capítulo explica, e de que o aluno precisa para seguir o texto, ganha a explicação no aposto de IA (seção 7), e só nele: fora do aposto, fica como o livro o usa, sem o sentido comum da palavra e sem o sentido tirado do uso.
5. **Sem imagens.** O mecanismo se explica com as palavras do livro, e nenhuma imagem entra, nem nos rótulos.
6. **As comparações que o livro faz separam o que se confunde:** tétano e botulismo (paralisia espástica e flácida); *Enterococcus* e *S. pneumoniae* na bancada; *N. gonorrhoeae* e *N. meningitidis* na vacina.
7. **A consequência prática que o livro dá aparece:** o que muda para quem cuida do paciente ou trabalha na bancada, como "os ensaios que procuram os genes de invasão **não discriminam** a *Shigella* da *E. coli* enteroinvasiva (EIEC)" e "quando o paciente infectado recebe alta, o leito deve ser cuidadosamente limpo".
8. **Números vêm dentro de frases que dizem o que significam:** "positiva em apenas cerca de 30% dos casos", "reduziu a mortalidade do botulismo de quase 70% para valores entre 5% e 10%".
9. **As etapas contam uma história só:** o agente (1), onde vive e quem atinge (2), como chega (3), como causa dano (4), o que esse dano provoca (5), como se confirma (6) e como se trata e previne (7). Quando der, o fim retoma o começo: "é justamente a falta desses reforços que deixa os idosos vulneráveis".

Quando o livro dá o porquê de um fato ou o que ele muda para o aluno, isso vai junto do fato, e não fica de fora numa frase seca que só o registra.

## 4. A Estrutura Canônica em 7 Etapas Investigativas

Todo documento responde, nesta ordem, às 7 etapas investigativas adaptadas do prefácio do Murray, com estes títulos exatos e os marcadores de colchetes `[ ]`:

1. **Identificação e Caracterização do Agente [QUAL AGENTE?]**
   - Classificação taxonômica, morfologia, coloração de Gram, arranjo, metabolismo, provas primárias bioquímicas e características distintivas da espécie.
2. **Reservatório e Hospedeiros Suscetíveis [ONDE E QUEM?]**
   - Reservatório natural (flora comensal, animais, meio ambiente) e grupos de risco/hospedeiros suscetíveis com seus respectivos fatores de vulnerabilidade.
3. **Mecanismos e Vias de Transmissão [QUANDO?]**
   - Vias de transmissão (contato, fômites, vetores, via endógena) e fatores desencadeantes (quebra de barreira, procedimentos invasivos, infecções prévias).
4. **Fatores de Virulência e Patogênese [POR QUÊ?]**
   - Fatores de virulência e mecanismos patogênicos (adesinas, cápsula, toxinas, enzimas hidrolíticas, formação de biofilme e evasão imune) explicados em sequência de ação.
5. **Manifestações Clínicas e Síndromes [O QUE CAUSA?]**
   - Doenças clínicas associadas agrupadas por fisiopatologia (mediadas por toxinas à distância, infecções purulentas locais e invasões sistêmicas profundas), manifestações sintomáticas e complicações.
6. **Diagnóstico Laboratorial [COMO TESTAR?]**
   - Diagnóstico laboratorial encadeado passo a passo: amostragem/coleta correta, microscopia (Gram), contaminações por comensais, meios de cultura (seletivos e diferenciais), provas bioquímicas e métodos moleculares (PCR/MALDI-TOF).
7. **Tratamento, Resistência e Profilaxia [COMO TRATAR E PREVENIR?]**
   - Evolução biológica dos mecanismos de resistência antimicrobiana, diferenciação entre cepas sensíveis e resistentes, esquemas terapêuticos indicados, intervenções cirúrgicas necessárias (drenagem de pus), contraindicações e medidas profiláticas.

- **O que precisa aparecer:** os pontos do quadro de resumo do capítulo para a bactéria (o bloco "RESUMOS Organismos clinicamente significativos", no começo de cada capítulo: palavras-chave, biologia e virulência, epidemiologia, doenças, diagnóstico e tratamento).
- **Tamanho:** o texto é curto, mas traz todas as informações necessárias; nada necessário sai só para caber num número de palavras. O aviso do conferidor de forma (fora de 850 a 2.100 palavras no corpo, sem os blocos de fonte) só pede um segundo olhar.
- **Etapa com pouco no livro:** fica com o pouco que o livro diz, sem nada de fora para encher.

## 5. Diretrizes de Formatação e Estilo

O esqueleto de todo texto:

```markdown
# Documento Investigativo Completo: O Caso do *Nome Científico*

**A Lógica do Estudo:** (a frase fixa abaixo)

---

### 1. Identificação e Caracterização do Agente [QUAL AGENTE?]

Texto da etapa.

> **Fonte Exata no Livro:** *Murray - Microbiologia Médica, Cap. N, p. X-Y*  
> *"Trecho literal do capítulo [...] outro trecho literal."*

---

### 2. Reservatório e Hospedeiros Suscetíveis [ONDE E QUEM?]

(e assim até a etapa 7, que termina no bloco de fonte; depois dela, só o rodapé da licença)
```

- **Título Principal (H1):** `# Documento Investigativo Completo: O Caso do *Nome Científico*`, com "do" ou "da" conforme o nome.
- **Subtítulo Metodológico:** sempre esta frase, igual em todos os textos:

  **A Lógica do Estudo:** Em vez de decorar listas isoladas, o estudo aplica o método investigativo do prefácio do livro, tratando o microrganismo como um "vilão" e a infecção como uma "cena de crime", detalhando **Qual** agente, **Onde** e **Quem**, **Quando**, **Por que** (armas/mecanismos), **O que** causa (sintomas/doenças) e **Como** testar, tratar e prevenir.

- **Etapas:** títulos `###` exatamente como na seção 4. Quando uma etapa tem grupos distintos (por exemplo, infecções intestinais e extraintestinais), usam-se subtítulos `####`, sem número. Não se usa `#####`.
- **Divisores de Seção:** uma linha `---` depois do subtítulo, entre uma etapa e a seguinte e no começo do rodapé da licença, em nenhum outro lugar.
- **Rodapé da Licença:** o texto termina, depois do bloco de fonte da etapa 7 e de uma linha em branco, no rodapé da licença, o do modelo `dados/rodape.md`. Ele não se escreve à mão: a peça do rodapé o põe no fim de cada documento, pelo comando de `dados/README.md`.
- **Listas:** `*` para itens paralelos; `1.` para sequências (passos de um mecanismo, pilares de um tratamento).
- **Ausência Absoluta de Emojis:** Nenhum ícone, emoji ou caractere gráfico decorativo é permitido em títulos, subtítulos, tabelas ou listas. Também não se usam fórmulas LaTeX; para setas, use "→".
- **Nomenclatura Botânica/Zoológica (Latim):** Nomes científicos de gêneros e espécies devem ser gravados obrigatoriamente em itálico (ex.: *Staphylococcus aureus*, *Escherichia coli*, *E. coli*), assim como os termos latinos (*in vivo*).
- **Destaques e Sinalização:** Utilizar negrito para termos de destaque, reagentes, nomes de exames, resultados de provas, porcentagens e genes.
- **Grafia:** "Gram-positivo" e "Gram-negativo"; temperaturas como "37 °C".
- **Citação em bloco (`>`):** só no bloco de fonte. Um quadro de comparação vai como texto comum, com rótulo em negrito.

## 6. Regras de Citação de Fontes e Rastreabilidade

Cada uma das 7 etapas termina com exatamente um bloco de fonte, que é a última coisa da etapa:

```markdown
> **Fonte Exata no Livro:** *Murray - Microbiologia Médica, Cap. N, p. X-Y*  
> *"Trecho literal do capítulo [...] outro trecho literal."*
```

- **Literal:** o trecho é copiado do `chapterNN.md` palavra por palavra, nunca reconstruído, resumido ou "arrumado". Partes omitidas são marcadas com `[...]` (ABNT NBR 10520, 5.2); aspas dentro do trecho viram aspas simples.
- **Páginas:** as do marcador `## p. N` que vem antes de cada parte citada: uma página (`p. 323`), um intervalo (`p. 323-324`) ou páginas separadas por vírgula (`p. 197, 213`). Nunca `&`.
- **Pertinente:** o trecho sustenta as afirmações principais da etapa.
- **Mais de um capítulo:** o trecho de outro capítulo, com o porquê de um fato ou a explicação de um termo (seção 3), entra no mesmo bloco, depois de uma linha `>` vazia, com a própria linha de referência, sem o rótulo **Fonte Exata no Livro**, que só a primeira citação do bloco leva:

  ```markdown
  > **Fonte Exata no Livro:** *Murray - Microbiologia Médica, Cap. N, p. X-Y*  
  > *"Trecho literal do capítulo da bactéria."*
  >
  > *Murray - Microbiologia Médica, Cap. M, p. Z*  
  > *"Trecho literal do outro capítulo."*
  ```

## 7. Regras Rigorosas de Integridade Conteudística

- **Proibição de Alteração de Fatos:** Informações científicas jamais podem ser distorcidas ou substituídas. Isso inclui intensificar ou atenuar: "geralmente não recomendado" não vira "nunca"; "até metade" não vira "a maioria".
- **O Livro Decide:** quando o texto e o livro divergem, vale o livro.
- **Só o que o livro diz:** cada fato, número, porquê e consequência vem do livro; nenhum porquê, consequência ou junção de passagens se deduz. O que não vem do livro só entra no aposto de IA, logo abaixo.
- **Aposto de IA:** quando nenhum capítulo explica um termo, uma sigla ou um conceito de que o aluno precisa para seguir o texto, a explicação curta vem logo depois dele, entre `[IA: ` e `]`, numa linha só; na sigla, o aposto é o nome completo, no lugar que a ABNT dá a ele, antes da sigla entre parênteses: `[IA: nome completo] (SIGLA)`. Ela pode trazer o fato geral que explica o termo, sem inventar (como o que é fagocitose), e nunca um fato da bactéria (número, epidemiologia, virulência, doença, diagnóstico, tratamento), um porquê ou uma consequência. O aposto não entra no bloco de fonte nem no glossário, e sai quando o livro der a explicação (seção 3, regra 4).
- **Quando o livro diverge** (uma passagem contra outra, o quadro de resumo contra o corpo do capítulo): a divergência vai para o arquivo de divergências do projeto, em `dados/`, pela peça da prateleira, e o texto ensina a forma que o arquivo dá como ensinada; enquanto ela não está no arquivo, o texto não escolhe nem junta as passagens, e o lugar dela é apontado na entrega do texto.
- **Preservação de Dados Numéricos:** Porcentagens de carreadores, especificidades, sensibilidades e taxas de resistência devem ser mantidas integralmente.
- **Consistência Inter-Tópicos:** Qualquer bactéria estudada posteriormente deverá seguir exatamente a mesma profundidade, o mesmo tom acadêmico-didático e a mesma estrutura aqui normatizada.

## 8. Checklist de Validação Antes de Salvar

- [ ] Título, subtítulo fixo e os 7 títulos de etapa exatamente como no modelo; `---` só entre as partes e no começo do rodapé da licença, no fim.
- [ ] Cada etapa abre com a frase de lógica e segue o padrão do tom (seção 3): rótulos, os porquês e as consequências que o livro dá, os termos com a explicação do livro entre parênteses e nenhuma imagem.
- [ ] Pontos do quadro de resumo do capítulo presentes.
- [ ] Cada termo técnico com a explicação que o livro dá, entre parênteses, na primeira vez em que aparece, e cada sigla, na primeira vez, entre parênteses, logo depois do nome completo que o livro dá; o que nenhum capítulo explica e o aluno precisa para seguir o texto, com o aposto de IA, só com o fato geral que o explica; fora do aposto, como o livro o usa.
- [ ] Explicação fluida do mecanismo biológico em substituição a listas secas.
- [ ] Nada que não esteja no livro, fora o aposto de IA, e nenhum porquê, consequência ou junção de passagens deduzidos; nenhuma informação sem uso; nenhum nome ou rota bioquímica só para mostrar.
- [ ] Cada divergência do livro como o arquivo de divergências a resolve, ou apontada na entrega, sem escolha nem junção no texto.
- [ ] Um bloco de fonte no fim de cada etapa, com trechos literais, `[...]` nas omissões, páginas conferidas no `chapterNN.md` e cada trecho de outro capítulo com a linha de referência dele (seção 6).
- [ ] Nomes em latim estritamente formatados em itálico; nenhuma palavra estrangeira solta; nenhum emoji.
- [ ] Nome do arquivo igual ao identificador da lista de controle (`controle-dos-textos.md`), em caixa baixa e com hifens (ex.: `staphylococcus-aureus.md`).

---

*Este documento está licenciado sob [CC BY-NC-SA 4.0](../LICENSE-CONTENT.txt).*
