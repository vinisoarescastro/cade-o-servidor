# Modelo do Arquivo CSV — Folha de Pagamento - Municipio de GoiÂNIA

> ⚠️ **Aviso:** Este modelo foi elaborado com base em uma **amostra parcial** do arquivo original. O documento completo pode conter outros valores, categorias, cargos, situações e variações não contempladas aqui. Campos descritos como exemplos refletem apenas os dados observados na amostra.

---

## Estrutura Geral

- Separador de colunas: **vírgula** (`,`)
- Campos de texto **sem aspas duplas** — nenhum campo vem entre aspas
- Campos monetários utilizam **ponto** (`.`) como separador decimal e **sem separador de milhar** — ex.: `1518.0`, `10450.01`
- **Matrícula exposta** sem mascaramento — ex.: `56688803`
- Datas no formato `DD/MM/AAAA`
- Cabeçalho presente na **primeira linha**
- Total de **10 colunas**

---

## Colunas

| # | Campo | Tipo | Exemplo | Descrição |
|---|-------|------|---------|-----------|
| 1 | `MATRICULA` | Inteiro | `56688803` | Matrícula funcional do servidor (sem mascaramento) |
| 2 | `NOME` | Texto | `ABADIA ALVES DE OLIVEIRA` | Nome completo do servidor (maiúsculas) |
| 3 | `CARGO` | Texto | `AUXILIAR EM SAÚDE` | Cargo ocupado pelo servidor |
| 4 | `LOCAL_TRABALHO` | Texto | `FUNDO PREVIDENCIARIO DO MUNICIPIO DE GOIANIA` | Unidade/local de trabalho do servidor |
| 5 | `TIPO_FOLHA` | Texto | `Folha Mensal` | Tipo da folha de pagamento do registro |
| 6 | `TIPO_ADMISSAO` | Texto | `NOMEADO EFETIVO E ESTAVEL (CONCURSADO)` | Tipo de admissão/vínculo funcional |
| 7 | `CARGA_HORARIA` | Texto | `135h Mensal` | Carga horária mensal do servidor |
| 8 | `SALARIO` | Decimal (ponto) | `1518.0` | Valor do salário/provento do registro (R$) |
| 9 | `DATA_ADMISSAO` | Data (`DD/MM/AAAA`) | `12/02/2008` | Data de admissão do servidor |
| 10 | `DATA_EXONERACAO_INATIVACAO` | Data (`DD/MM/AAAA`) ou vazio | `25/04/2026` / `` | Data de exoneração ou inativação (vazio se ainda ativo) |

---

## Observações

- Nenhum campo utiliza aspas duplas, independentemente do conteúdo.
- Campos monetários usam **ponto** como decimal (ex.: `1518.0`, `81339.45`), ao contrário dos arquivos anteriores que usavam vírgula.
- Não há separador de milhar nos valores numéricos.
- Um mesmo servidor pode aparecer em **múltiplas linhas**, uma para cada tipo de folha (Mensal, Décimo Terceiro, Diferença, Seção Extraordinária, Férias).
- O campo `DATA_EXONERACAO_INATIVACAO` fica **vazio** para servidores ainda ativos e preenchido para contratos com data de fim definida ou servidores já desligados.
- O campo `SALARIO` pode variar entre linhas do mesmo servidor dependendo do `TIPO_FOLHA` — por exemplo, o valor da `Seção Extraordinária` pode diferir do valor da `Folha Mensal`.
- Os exemplos de valores, cargos, locais de trabalho e admissões presentes neste documento refletem **somente a amostra analisada**. O arquivo completo pode apresentar novos cargos, locais, tipos de admissão e outros valores não previstos aqui.

---

## Exemplo de Linha

```
129406703,ABADIA APARECIDA DAS CHAGAS,AUXILIAR DE ATIVIDADES EDUCATIVAS,EDUCANDARIO NEIO LUCIO NACIFF.,Folha Mensal,CONTRATO ADMINISTRATIVO POR TEMPO DETERMINADO,135h Mensal,1803.74,26/04/2024,25/04/2026
```

---

## Valores observados na amostra

> ⚠️ Listas **não exaustivas** — o documento completo pode conter outros valores.

### Tipo de Folha (`TIPO_FOLHA`)
- `Folha Mensal`
- `Folha Décimo Terceiro`
- `Folha Diferença`
- `Seção Extraordinária`
- `Férias`

### Tipo de Admissão (`TIPO_ADMISSAO`)
- `NOMEADO EFETIVO E ESTAVEL (CONCURSADO)`
- `CONTRATO ADMINISTRATIVO POR TEMPO DETERMINADO`
- `APOSENTADO POR TEMPO DE SERVICO`
- `APOSENTADO POR TEMPO DE SERVICO (PROPORCIONAL)`
- `APOSENTADORIA POR INVALIDEZ PROPORCIONAL`
- `APOSENTADORIA VOLUNTÁRIA INTEGRAL`
- `PENSIONISTA`
- `PENSIONISTA PROPORCIONAL`
- `PENSIONISTA PROPORCIONAL COM COMP. DE MINIMO`

### Carga Horária (`CARGA_HORARIA`)
- `120h Mensal`
- `135h Mensal`
- `180h Mensal`