# Modelo do Arquivo CSV — Folha de Pagamento - Estado de Goiás

> ⚠️ **Aviso:** Este modelo foi elaborado com base em uma **amostra parcial** do arquivo original. O documento completo pode conter outros valores, categorias, cargos, situações e variações não contempladas aqui. Campos descritos como exemplos refletem apenas os dados observados na amostra.

---

## Estrutura Geral

- Separador de colunas: **vírgula** (`,`)
- Campos de texto com vírgula no conteúdo vêm entre **aspas duplas** — ex.: `"SECRETARIA DE ESTADO DE CIÊNCIA, TECNOLOGIA E INOVAÇÃO"`
- Campos monetários com decimais vêm entre **aspas duplas** e usam **vírgula** como separador decimal — ex.: `"7977,58"`
- Campos monetários com valores inteiros **não** vêm entre aspas — ex.: `0`, `5695`, `3780`
- **CPF parcialmente mascarado** — ex.: `*524101**`
- Cabeçalho presente na **primeira linha**

---

## Colunas

| # | Campo | Tipo | Exemplo | Descrição |
|---|-------|------|---------|-----------|
| 1 | `Descricao_Mes_Ano` | Texto | `Dezembro de  2025` | Mês e ano de referência da folha (note o duplo espaço antes do ano) |
| 2 | `Nome_Orgao` | Texto | `SECRETARIA DE ESTADO DA EDUCAÇÃO` | Nome do órgão principal do servidor |
| 3 | `Nome_Unidade_Orgao` | Texto | `GERENCIA DE FOLHA DE PAGAMENTO DE BENEFÍCIOS` | Nome da unidade dentro do órgão |
| 4 | `CPF_Formatado` | Texto mascarado | `*524101**` | CPF do servidor com dígitos ocultos |
| 5 | `Nome_Servidor` | Texto | `VIGILATO PORTO SILVERIO` | Nome completo do servidor (maiúsculas) |
| 6 | `Nome_Departamento_Orgao` | Texto | `DIRETORIA DE PREVIDÊNCIA` | Departamento do órgão ao qual o servidor está vinculado |
| 7 | `Nome_Cargo_2` | Texto | `Professor - IV` | Denominação do cargo (pode conter nível e número de lei) |
| 8 | `Descricao_Nivel_Salarial` | Texto | `E` / `CII` / `Não se Aplica` | Nível salarial do servidor |
| 9 | `Descricao_Simbolo_Cargo_2` | Texto | `P - IV` / `PCR` / `AFRE` | Símbolo/código do cargo |
| 10 | `Nome_Cargo` | Texto | `Não se Aplica` | Nome do cargo secundário (frequentemente `Não se Aplica`) |
| 11 | `Descricao_Nivel_Salarial_Secundario` | Texto | `Não se Aplica` | Nível salarial secundário (frequentemente `Não se Aplica`) |
| 12 | `Descricao_Tipo_Vinculo_Agrupado` | Texto | `EFETIVO` | Tipo de vínculo funcional do servidor |
| 13 | `Data_Admissao` | Data (`DD/MM/AAAA`) ou vazio | `01/01/2025` / `` | Data de admissão (pode estar vazio) |
| 14 | `Data_Exoneracao` | Data (`DD/MM/AAAA`) ou vazio | `` | Data de exoneração (pode estar vazio) |
| 15 | `Numero_Carga_Horaria_Servidor` | Inteiro ou vazio | `200` / `150` / `` | Carga horária mensal em horas (pode estar vazio) |
| 16 | `Valor_Provento_Ferias_Com_Desconto` | Decimal (vírgula, entre aspas) ou inteiro | `"7977,58"` / `5695` | Valor do provento de férias com desconto (R$) |
| 17 | `Valor_Ferias_Mais_Um_Terco_Ferias` | Decimal ou inteiro | `0` | Valor de férias acrescido de 1/3 (R$) |
| 18 | `Valor_Decimo_Terceiro` | Decimal ou inteiro | `0` | Valor do 13º salário (R$) |
| 19 | `Valor_Provento` | Decimal (vírgula, entre aspas) ou inteiro | `"7977,58"` / `5695` | Valor total dos proventos (R$) |
| 20 | `Valor_Corte_Teto` | Decimal ou inteiro | `0` / `3780` | Valor do corte de teto constitucional (R$) |
| 21 | `Valor_Corte_Teto_Com_Desconto` | Decimal (vírgula, entre aspas) ou inteiro | `"6262,24"` / `0` | Valor do corte de teto após descontos (R$) |
| 22 | `Valor_Liquido` | Decimal (vírgula, entre aspas) ou inteiro | `"1715,34"` / `0` | Valor líquido a receber (R$) |

---

## Observações

- O campo `Descricao_Mes_Ano` apresenta **duplo espaço** entre o mês e o ano — ex.: `Dezembro de  2025`.
- O **CPF é mascarado**, com dígitos centrais visíveis e extremidades ocultas por asteriscos — ex.: `*524101**`.
- Os campos `Nome_Cargo`, `Descricao_Nivel_Salarial_Secundario` aparecem frequentemente como `Não se Aplica` na amostra, mas podem ter outros valores no arquivo completo.
- Os campos `Data_Admissao`, `Data_Exoneracao` e `Numero_Carga_Horaria_Servidor` podem estar **completamente vazios**.
- Valores monetários **inteiros** (ex.: `0`, `5695`, `3780`) aparecem **sem aspas**; valores com casas decimais (ex.: `"7977,58"`) aparecem **entre aspas duplas**.
- Um mesmo servidor pode aparecer em **múltiplas linhas** com cargos diferentes (ex.: dois cargos distintos de REQUISITADO).
- O campo `Nome_Orgao` pode conter vírgula no nome — nesses casos vem entre aspas duplas.
- Os exemplos de valores, cargos, lotações e categorias presentes neste documento refletem **somente a amostra analisada**. O arquivo completo pode apresentar novos órgãos, cargos, vínculos, níveis salariais e outros valores não previstos aqui.

---

## Exemplo de Linha

```
Dezembro de  2025,SECRETARIA DE ESTADO DA EDUCAÇÃO,GERENCIA DE FOLHA DE PAGAMENTO DE BENEFÍCIOS,*524101**,VIGILATO PORTO SILVERIO,DIRETORIA DE PREVIDÊNCIA,Professor - IV,E,P - IV,Não se Aplica,Não se Aplica,PENSIONISTA,,,200,"7977,58",0,0,"7977,58",0,"6262,24","1715,34"
```

---

## Valores observados na amostra

> ⚠️ Listas **não exaustivas** — o documento completo pode conter outros valores.

### Tipo de Vínculo (`Descricao_Tipo_Vinculo_Agrupado`)
- `EFETIVO`
- `PENSIONISTA`
- `APOSENTADO`
- `REQUISITADO`

### Carga Horária (`Numero_Carga_Horaria_Servidor`)
- `120`
- `135`
- `150`
- `200`
- `210`
- `220`
- vazio

### Órgãos observados (`Nome_Orgao`)
- `SECRETARIA DE ESTADO DA EDUCAÇÃO`
- `SECRETARIA DE ESTADO DA SAÚDE`
- `SECRETARIA DE ESTADO DA ECONOMIA`
- `SECRETARIA DE ESTADO DA ADMINISTRAÇÃO`
- `SECRETARIA DE ESTADO DE DESENVOLVIMENTO SOCIAL`
- `SECRETARIA DE ESTADO DE CIÊNCIA, TECNOLOGIA E INOVAÇÃO`
- `DELEGACIA-GERAL DA POLÍCIA CIVIL`
- `POLÍCIA MILITAR`
- `CONTROLADORIA-GERAL DO ESTADO`
- `PROCURADORIA-GERAL DO ESTADO`
- `UNIVERSIDADE ESTADUAL DE GOIÁS - UEG`