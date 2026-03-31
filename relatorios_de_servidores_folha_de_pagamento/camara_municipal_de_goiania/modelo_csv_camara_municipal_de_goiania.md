# Modelo do Arquivo CSV — Folha de Pagamento - Câmara Municipal de Goiânia

> ⚠️ **Aviso:** Este modelo foi elaborado com base em uma **amostra parcial** do arquivo original. O documento completo pode conter outros valores, categorias, cargos, situações e variações não contempladas aqui. Campos descritos como exemplos refletem apenas os dados observados na amostra.

---

## Estrutura Geral

- Separador de colunas: **ponto e vírgula** (`;`)
- Campos de texto podem vir entre **aspas duplas** (`"`)
- Campos monetários utilizam **vírgula** (`,`) como separador decimal e **ponto** (`.`) como separador de milhar — ex.: `28.937,08`
- Carga horária utiliza **vírgula** como separador decimal — ex.: `30,0`
- Cabeçalho presente na **primeira linha**

---

## Colunas

| # | Campo | Tipo | Exemplo | Descrição |
|---|-------|------|---------|-----------|
| 1 | `Matrícula` | Inteiro | `55686334928` | Matrícula funcional do servidor |
| 2 | `Nome` | Texto (entre aspas) | `"AAVA SANTIAGO AGUIAR"` | Nome completo do servidor (maiúsculas) |
| 3 | `Situação` | Texto | `ATIVO` | Situação funcional do servidor |
| 4 | `Órgão` | Texto (entre aspas) | `"PODER LEGISLATIVO"` | Órgão ao qual o servidor pertence |
| 5 | `Cargo` | Texto (entre aspas) | `"ASSESSOR PARLAMENTAR DE GABINETE VI"` | Cargo ocupado pelo servidor |
| 6 | `Lotação` | Texto (entre aspas) | `"GABINETE DE AAVA SANTIAGO"` | Setor/lotação do servidor |
| 7 | `Decreto Nomeação` | Texto (entre aspas) | `"ATA 1"` / `1148` / `"PORTARIA 76"` | Decreto ou portaria de nomeação |
| 8 | `Estabilidade` | Texto ou `-` | `-` | Informação de estabilidade (pode ser `-`) |
| 9 | `Data Admissão` | Data (`DD/MM/AAAA`) | `01/01/2025` | Data de admissão do servidor |
| 10 | `Tipo de Admissão` | Texto | `COMISSIONADO` | Tipo de admissão do servidor |
| 11 | `Carga Horária` | Decimal (vírgula) | `30,0` | Carga horária semanal |
| 12 | `Referência` | Texto | `Dezembro/2025` | Mês e ano de referência da folha |
| 13 | `Tipo Pagamento` | Texto (entre aspas) | `MENSAL` | Tipo do pagamento do registro |
| 14 | `Movimentação` | Texto | `NORMAL` | Tipo de movimentação do registro |
| 15 | `Salário Base` | Decimal (vírgula) | `8.912,16` | Salário base do servidor (R$) |
| 16 | `Proventos` | Decimal (vírgula) | `11.200,65` | Total de proventos/vencimentos (R$) |
| 17 | `Descontos` | Decimal (vírgula) | `2.232,03` | Total de descontos (R$) |
| 18 | `Liquido` | Decimal (vírgula) | `8.968,62` | Valor líquido a receber (R$) |
| 19 | `Função` | Texto ou vazio | `` | Função desempenhada (pode estar vazio) |

---

## Observações

- O arquivo utiliza **ponto e vírgula** (`;`) como separador, diferente do padrão CSV com vírgula.
- Campos de texto geralmente vêm entre **aspas duplas**, incluindo nome, órgão, cargo, lotação e tipo de pagamento.
- O campo `Decreto Nomeação` pode conter texto (`"ATA 1"`, `"PORTARIA 76"`) ou número puro (`1148`, `925`).
- Um mesmo servidor pode aparecer em **múltiplas linhas**, uma para cada tipo de pagamento (MENSAL, FÉRIAS, 13º SALÁRIO, RESCISÃO).
- O campo `Salário Base` pode ser `0,00` em registros de FÉRIAS, 13º SALÁRIO ou RESCISÃO.
- O campo `Função` pode estar **vazio** ao final da linha.
- Os exemplos de valores, cargos, lotações e categorias presentes neste documento refletem **somente a amostra analisada**. O arquivo completo pode apresentar novos cargos, lotações, tipos de pagamento, situações e outros valores não previstos aqui.

---

## Exemplo de Linha

```
55686334027;"ADAIR CORDEIRO VASCO";ATIVO;"PODER LEGISLATIVO";"ASSESSOR PARLAMENTAR DE GABINETE I";"GABINETE DE DENICIO TRINDADE";"PORTARIA 36";-;01/01/2025;COMISSIONADO;30,0;Dezembro/2025;MENSAL;NORMAL;8.912,16;11.200,65;2.232,03;8.968,62;
```

---

## Valores observados na amostra

> ⚠️ Listas **não exaustivas** — o documento completo pode conter outros valores.

### Situação
- `ATIVO`
- `RESCINDIDO`

### Tipo de Admissão
- `COMISSIONADO`
- `VEREADOR`

### Tipo de Pagamento
- `MENSAL`
- `FÉRIAS`
- `13º SALÁRIO`
- `RESCISÃO`

### Movimentação
- `NORMAL`