# Modelo do Arquivo CSV — Folha de Pagamento - Assembleia de Goiás

> ⚠️ **Aviso:** Este modelo foi elaborado com base em uma **amostra parcial** do arquivo original. O documento completo pode conter outros valores, categorias, cargos, vínculos e variações não contempladas aqui. Campos descritos como exemplos refletem apenas os dados observados na amostra.

---

## Estrutura Geral

O arquivo é separado por **vírgulas** (`,`) e possui **cabeçalho na primeira linha**.

---

## Colunas

| # | Campo | Tipo | Exemplo | Descrição |
|---|-------|------|---------|-----------|
| 1 | `id` | Inteiro | `682494` | Identificador único do registro |
| 2 | `ano` | Inteiro | `2025` | Ano de referência da folha |
| 3 | `mes` | Inteiro | `12` | Mês de referência da folha |
| 4 | `matricula` | Inteiro | `503894563` | Matrícula funcional do servidor |
| 5 | `nome` | Texto | `ABADIA DA PENHA ALVES...` | Nome completo do servidor (maiúsculas) |
| 6 | `admissao` | Data (`DD/MM/AAAA`) | `01/12/2024` | Data de admissão |
| 7 | `desligamento` | Data (`DD/MM/AAAA`) ou vazio | `""` | Data de desligamento (vazio se ativo) |
| 8 | `cargo` | Texto | `ASSESSOR NIVEL II` | Cargo ocupado |
| 9 | `funcao` | Texto ou `-` | `-` | Função desempenhada (pode ser `-`) |
| 10 | `vinculo` | Texto | `COMISSIONADOS` | Tipo de vínculo funcional |
| 11 | `carga_horaria` | Texto ou `-` | `30H` | Carga horária semanal (pode ser `-`) |
| 12 | `status` | Texto ou `-` | `-` | Status do servidor (pode ser `-`) |
| 13 | `remuneracao_bruta` | Decimal | `1872.72` | Remuneração bruta (R$) |
| 14 | `descontos` | Decimal | `145.77` | Total de descontos (R$) |
| 15 | `remuneracao_liquida` | Decimal | `1726.95` | Remuneração líquida (R$) |
| 16 | `diferencas` | Decimal | `0.0` | Diferenças/ajustes (R$) |
| 17 | `lotacao` | Texto | `Gabinete Parlamentar` | Setor/lotação do servidor |
| 18 | `padrao_classe` | Texto ou `-` | `AL-31` | Padrão/classe do cargo (pode ser `-`) |
| 19 | `ferias` | Decimal | `0.0` | Valor de férias (R$) |
| 20 | `corte` | Decimal | `0.0` | Valor de corte (R$) |
| 21 | `decimo_terceiro` | Decimal | `790.59` | Valor do 13º salário (R$) |
| 22 | `auxilio_alimentacao` | Decimal | `3000.0` | Auxílio-alimentação (R$) |
| 23 | `auxilio_transporte` | Decimal | `0.0` | Auxílio-transporte (R$) |
| 24 | `indenizacoes` | Decimal | `0.0` | Indenizações (R$) |
| 25 | `classe` | Texto ou `-` | `Singular - ANALISTA LEGISLATIVO` | Descrição da classe (pode ser `-`) |

---

## Observações

- Campos monetários utilizam ponto (`.`) como separador decimal.
- Campos ausentes ou não aplicáveis são representados por `-` ou `""` (string vazia entre aspas duplas).
- O campo `lotacao` pode conter vírgulas; nesses casos, o valor vem entre aspas duplas — ex.: `"Procuradoria de Orçamento, Finanças e Controle Externo"`.
- Datas seguem o formato `DD/MM/AAAA`.
- O campo `nome` sempre em letras maiúsculas.
- Os exemplos de valores, cargos, lotações e categorias presentes neste documento refletem **somente a amostra analisada**. O arquivo completo pode apresentar novos cargos, lotações, padrões de classe, formatos de data, vínculos e outros valores não previstos aqui.

---

## Exemplo de Linha

```
682494,2025,12,503894563,ABADIA DA PENHA ALVES PEREIRA DOS SANTOS,01/12/2024,"",ASSESSOR NIVEL II,-,COMISSIONADOS,30H,-,1872.72,145.77,1726.95,0.0,Gabinete Parlamentar,-,0.0,0.0,790.59,3000.0,0.0,0.0,-
```

## Tipos de Vínculo observados na amostra

> ⚠️ Lista **não exaustiva** — o documento completo pode conter outros tipos de vínculo.

- `COMISSIONADOS`
- `DEPUTADOS`
- `APOSENTADOS`
- `EFETIVOS PREVIDÊNCIA COMPLEMENTAR`