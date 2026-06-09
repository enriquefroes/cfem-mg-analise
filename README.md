# CFEM Minas Gerais — Análise Exploratória (2017–2026)

Análise da arrecadação de CFEM (Compensação Financeira pela Exploração de Recursos Minerais) nos principais municípios mineradores de Minas Gerais, desenvolvida em 5 notebooks Python para Google Colab.

---

## Sobre o projeto

A CFEM é o royalty pago pelas empresas mineradoras ao governo pela extração de recursos minerais. Este projeto analisa como essa arrecadação se distribui entre os municípios de Minas Gerais, como evoluiu ao longo do tempo e qual o seu peso na economia local em relação ao PIB municipal.

Destaques da análise:
- Ranking dos maiores municípios arrecadadores em dois períodos (2017–2021 e 2022–2026)
- Impacto do rompimento da barragem B1 de Brumadinho (jan/2019) na arrecadação
- Relação CFEM × PIB municipal para medir dependência da mineração
- Composição por substância mineral (ferro, ouro e demais)

---

## Estrutura do repositório

```
cfem-mg-analise/
│
├── NB1_Exploracao_Limpeza.ipynb          # Leitura, limpeza e exportação dos dados
├── NB2_Ranking_Municipios_MG.ipynb       # Ranking e comparativo com PIB
├── NB3_Evolucao_Temporal.ipynb           # Série temporal e sazonalidade
├── NB4_Brumadinho_Analise.ipynb          # Impacto do rompimento
├── NB5_Substancias_Minerais.ipynb        # Análise por substância mineral
└── README.md
```

> Os arquivos de dados brutos (CFEM e PIB) não estão no repositório por conta do tamanho. Veja a seção **Dados** abaixo para baixá-los.

---

## Resultados

### Ranking CFEM — Top 10 municípios de MG (2022–2026)
> Conceição do Mato Dentro lidera com R$ 1,73 bilhão acumulado. Belo Vale e Brumadinho saíram do top 10 em relação ao período anterior, reflexo do rompimento de 2019.

### CFEM como % do PIB municipal
> São Gonçalo do Rio Abaixo, Conceição do Mato Dentro e Itatiaiuçu apresentam os maiores ratios — municípios onde a mineração representa parcela significativa da economia local.

### Impacto de Brumadinho
> A média mensal de CFEM caiu após janeiro de 2019. A análise estima a perda acumulada de royalties comparando com a média histórica pré-rompimento.

### Composição mineral
> O minério de ferro responde pela maior parte de toda a arrecadação CFEM de Minas Gerais no período analisado.

---

## Dados

| Arquivo | Fonte | Período | Download |
|---|---|---|---|
| `CFEM_Arrecadacao_2017_2021.xlsx` | ANM — Agência Nacional de Mineração | 2017–2021 | [sistemas.anm.gov.br](https://sistemas.anm.gov.br) |
| `CFEM_Arrecadacao_2022_2026.csv` | ANM — Agência Nacional de Mineração | 2022–2026 | [sistemas.anm.gov.br](https://sistemas.anm.gov.br) |
| PIB Municipal 2021 e 2023 | IBGE — PIB dos Municípios | 2021, 2023 | [ibge.gov.br](https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9088-produto-interno-bruto-dos-municipios.html) |
| População | IBGE — Censo Demográfico 2022 | 2022 | [ibge.gov.br](https://www.ibge.gov.br/estatisticas/sociais/populacao/22827-censo-demografico-2022.html) |

---

## Tecnologias

| Tecnologia | Versão | Uso |
|---|---|---|
| Python | 3.10+ | Linguagem principal |
| pandas | 1.5+ | Manipulação e agregação dos dados |
| matplotlib | 3.6+ | Geração de todos os gráficos |
| numpy | 1.23+ | Cálculos numéricos e indexação |
| Google Colab | — | Ambiente de execução dos notebooks |
| Google Drive | — | Armazenamento persistente dos dados e saídas |

Todas as bibliotecas já vêm instaladas por padrão no Google Colab — não é necessário instalar nada.

---

## ▶️ Como executar

### Pré-requisitos
- Conta Google (para usar o Colab e o Drive)
- Arquivos de dados baixados (links na seção Dados acima)

### Passo a passo

**1.** Crie uma pasta chamada `CFEM Minas Gerais` no seu Google Drive

**2.** Faça upload dos arquivos de dados e dos 5 notebooks para essa pasta

**3.** Abra o `NB1_Exploracao_Limpeza.ipynb` no Google Colab, execute todas as células — ele vai:
   - Montar o Drive automaticamente (pedirá permissão na primeira célula)
   - Ler os arquivos brutos
   - Gerar os arquivos limpos em `CFEM Minas Gerais/dados_processados/`

**4.** A partir daí, os notebooks NB2 a NB5 podem ser executados em qualquer ordem e em qualquer sessão futura — eles leem os dados limpos diretamente do Drive

**5.** Todos os gráficos são salvos automaticamente em `CFEM Minas Gerais/graficos/`

---

## Fontes — ABNT

AGÊNCIA NACIONAL DE MINERAÇÃO (Brasil). **Sistema de Informações Geográficas da Mineração — SIGMINE: arrecadação CFEM**. Brasília: ANM, 2026. Disponível em: https://sistemas.anm.gov.br. Acesso em: 7 jun. 2026.

INSTITUTO BRASILEIRO DE GEOGRAFIA E ESTATÍSTICA. **PIB dos municípios: 2021**. Rio de Janeiro: IBGE, 2023. Disponível em: https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9088-produto-interno-bruto-dos-municipios.html. Acesso em: 7 jun. 2026.

INSTITUTO BRASILEIRO DE GEOGRAFIA E ESTATÍSTICA. **PIB dos municípios: 2023**. Rio de Janeiro: IBGE, 2025. Disponível em: https://www.ibge.gov.br/estatisticas/economicas/contas-nacionais/9088-produto-interno-bruto-dos-municipios.html. Acesso em: 7 jun. 2026.

INSTITUTO BRASILEIRO DE GEOGRAFIA E ESTATÍSTICA. **Censo Demográfico 2022: resultados do universo**. Rio de Janeiro: IBGE, 2023. Disponível em: https://www.ibge.gov.br/estatisticas/sociais/populacao/22827-censo-demografico-2022.html. Acesso em: 7 jun. 2026.

---

## Licença

Este projeto está sob a licença MIT. Os dados utilizados são públicos e de acesso livre conforme disponibilizados pela ANM e pelo IBGE.
