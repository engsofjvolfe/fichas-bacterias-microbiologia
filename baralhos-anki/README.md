# Baralho do Anki das bactérias

O `bacterias.apkg` é um baralho do Anki feito da tabela dos patógenos em palavras-chave,
[documentos-gerados/tabela.md](../documentos-gerados/tabela.md). A tabela tem 24 agentes, e
cada um dá cinco cartões, um por coluna de conteúdo: Doença Típica, Onde / Status, Quem, Fator
de Virulência e Tratamento. São 120 cartões. As colunas #, Agente e Fonte não viram cartão:
são o número da linha, o nome do agente e o arquivo do texto de estudo daquela linha.

Cada cartão traz, na frente, uma pergunta e, no verso, a resposta, escrita pelo texto de estudo
do agente, e o trecho do texto que a sustenta, com o nome do arquivo entre colchetes.
O pacote sai da tabela e dos textos por programa, sempre o mesmo para o mesmo CSV, e
reimportar o pacote atualiza os cartões em vez de duplicá-los.

## Os arquivos

| Arquivo | O que é |
| --- | --- |
| `bacterias.apkg` | o baralho, para importar no Anki |
| `bacterias.csv` | um cartão por linha, com a pergunta (`pergunta`), a resposta (`resposta`), as palavras-chave da célula (`palavras_chave`) e o trecho (`trecho`) de cada um |
| [`dados/baralho-anki.json`](../dados/baralho-anki.json) | a configuração: as colunas da tabela, as marcas de ênfase, o nome do baralho, o tipo de nota e a data da versão |
| `dados/baralho-anki-frente.html`, `dados/baralho-anki-verso.html` e `dados/baralho-anki-estilo.css` | os modelos da frente e do verso do cartão e o estilo dele |
| [`dados/baralho-anki-conferido.json`](../dados/baralho-anki-conferido.json) | o sha256 da tabela e de cada texto de estudo na última conferência de conteúdo dos cartões |

## Como os cartões se fazem

Nada entra num cartão que não esteja no texto de estudo do agente: nem na pergunta, nem na
resposta. O que é clássico em outros livros e não está no texto fica de fora.

- **Pergunta (`pergunta`, na frente):** uma pergunta que a célula responde por inteiro (todas
  as palavras-chave dela) e que não entrega a resposta. Quando o texto dá o porquê de um item,
  a pergunta pede o porquê, e o trecho o mostra.
- **Resposta (`resposta`, no verso):** escrita, e não copiada, para explicar o que o texto diz,
  só com o necessário para responder: cada parte da pergunta, na ordem dela, em uma a três
  frases, com as palavras-chave da célula em negrito. A regra maior é dizer só o que ensina, da
  forma mais simples que o rigor permite: um número ou um nome (de enzima, de substância, de
  via) só entra quando é ele que responde à pergunta. Não intensifica nem atenua o texto ("pode
  formar" continua "pode formar"), não traz o que a pergunta não pede e só repete a explicação
  de um termo quando a resposta não se entende sem ela.
- **Palavras-chave (`palavras_chave`):** a célula da tabela, copiada pelo programa, sem
  reescrever; ficam no CSV, e não no cartão, porque a resposta traz todas elas.
- **Trecho (`trecho`, no verso, abaixo da resposta):** uma ou duas frases copiadas letra por
  letra do texto de estudo, de preferência do corpo da etapa, e não do bloco de fonte do livro,
  que sustentam a pergunta.

Todo texto tem as sete etapas do manual de consistência, com os mesmos títulos. Doença Típica
sai da etapa 5; Onde / Status, da 2; Quem, da 2 e da 3; Fator de Virulência, da 4; e
Tratamento, da 7. O trecho de cada cartão se procura nessa etapa.

| Coluna | A pergunta | O raciocínio que ela pede |
| --- | --- | --- |
| Doença Típica | um caso ou uma pista clínica do texto, e a pergunta pelas doenças típicas | o que liga a doença ao mecanismo ou ao local |
| Onde / Status | onde a bactéria vive e qual o status, com a consequência que o texto dá | por que achar a bactéria numa amostra nem sempre é doença |
| Quem | quem mais adoece e por quê | a defesa que falta ou a exposição que pesa |
| Fator de Virulência | o efeito descrito no texto, e a pergunta pelos fatores que o explicam | o que cada fator faz |
| Tratamento | a conduta, com o porquê que o texto dá | por que um antibiótico não serve ou por que o prazo importa |

## Como se refaz

As ferramentas são da peça [baralho-anki](https://github.com/engsofjvolfe/prateleira-itens-agnosticos/tree/main/baralho-anki)
da prateleira, o repositório de peças que este projeto usa. Ela fica na pasta `prateleira/`,
na raiz do projeto, fora do git dele:

    git clone https://github.com/engsofjvolfe/prateleira-itens-agnosticos.git prateleira

O README da peça diz o que cada script recebe e entrega e o que cada `ERRO` quer dizer. Da raiz
do projeto:

1. O registro da conferência de conteúdo diz que texto mudou desde ela; só os cartões daquele
   agente se conferem de novo, contra o texto dele, lido inteiro:

       python3 -I prateleira/baralho-anki/conferido.py dados/baralho-anki.json documentos-gerados/tabela.md dados/baralho-anki-conferido.json --pasta documentos-gerados

2. O CSV, a partir da tabela; a pergunta, a resposta e o trecho de cada cartão que continua
   ficam como estavam, e as linhas novas vêm com os três vazios, que se escrevem pelo texto do
   agente:

       python3 -I prateleira/baralho-anki/gera_csv.py dados/baralho-anki.json documentos-gerados/tabela.md baralhos-anki/bacterias.csv

3. A conferência do CSV, que precisa sair com `0 erro(s)`: cada linha contra a tabela, cada
   trecho no texto de estudo e cada campo contra os padrões proibidos, as marcas de IA da
   prateleira e os deste projeto:

       python3 -I prateleira/baralho-anki/confere_baralho.py dados/baralho-anki.json documentos-gerados/tabela.md baralhos-anki/bacterias.csv --pasta documentos-gerados --proibidos prateleira/confere-forma/marcas-de-ia.json --proibidos dados/confere-forma-proibidos.json

4. O pacote, com uma `data` nova em `dados/baralho-anki.json` a cada versão nova do CSV:

       python3 -I prateleira/baralho-anki/gera_apkg.py dados/baralho-anki.json baralhos-anki/bacterias.csv baralhos-anki/bacterias.apkg --frente dados/baralho-anki-frente.html --verso dados/baralho-anki-verso.html --estilo dados/baralho-anki-estilo.css

5. Depois de conferido o conteúdo dos cartões, o registro se grava de novo:

       python3 -I prateleira/baralho-anki/conferido.py dados/baralho-anki.json documentos-gerados/tabela.md dados/baralho-anki-conferido.json --pasta documentos-gerados --gravar

A conferência de conteúdo de agora é a de 2026-11-03: cada célula das 24 linhas da tabela e
cada cartão conferidos contra o texto de estudo do agente, lido inteiro.
