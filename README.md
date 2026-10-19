# Dashboard Interativa de Vendas Porsche

## Sobre o projeto

Este projeto tem como objetivo desenvolver uma dashboard interativa em HTML para análise de vendas da Porsche, transformando dados tabulares em indicadores e visualizações que facilitem a interpretação do desempenho comercial.

A iniciativa faz parte de um desafio prático da DIO, no qual são aplicados conceitos de tratamento de dados, análise de negócio, construção de dashboards com auxílio de inteligência artificial e publicação de aplicações estáticas na web.

A proposta é desenvolver uma página com indicadores de desempenho, gráficos e filtros interativos, permitindo explorar os registros de vendas sob diferentes perspectivas.

## Objetivos

- Analisar o desempenho comercial por modelo de veículo.
- Identificar os estados com maior volume de vendas.
- Compreender a distribuição das vendas por método de pagamento.
- Apresentar indicadores gerais, como quantidade de vendas, receita total e ticket médio.
- Criar filtros para explorar diferentes recortes dos dados.
- Desenvolver uma interface visual organizada e coerente com a identidade da marca Porsche.
- Publicar a dashboard utilizando o GitHub Pages.

## Perguntas de negócio

A dashboard será estruturada para responder a três perguntas principais.

### 1. Quais modelos de Porsche geram maior receita?

**Visualização proposta:** gráfico de barras com a receita total agrupada por modelo.

Essa análise permite identificar quais modelos concentram a maior parcela do valor total vendido e comparar sua participação no resultado comercial.

### 2. Quais estados apresentam o maior volume de vendas?

**Visualização proposta:** gráfico de barras com a quantidade de vendas por estado.

O objetivo é identificar a distribuição geográfica dos registros e destacar os estados com maior concentração de vendas na base analisada.

### 3. Quais métodos de pagamento são mais utilizados?

**Visualização proposta:** gráfico de barras ou gráfico de rosca com a quantidade de vendas por método de pagamento.

Essa análise permite observar a frequência de utilização das diferentes modalidades de pagamento presentes nos registros.

## Indicadores principais

A proposta prevê os seguintes indicadores no topo da dashboard:

- **Total de vendas:** quantidade de registros considerados na análise.
- **Receita total:** soma dos preços de venda válidos.
- **Ticket médio:** receita total dividida pela quantidade de vendas consideradas, desde que haja registros válidos.

Os indicadores deverão acompanhar os filtros aplicados, de modo que os valores apresentados representem o conjunto de dados selecionado pelo usuário.

## Filtros interativos

A dashboard deverá contar com filtros para permitir a exploração dos dados por diferentes dimensões:

- Modelo Porsche.
- Estado.
- Método de pagamento.
- Status de entrega.

Os filtros deverão atualizar os indicadores e os gráficos de forma consistente, respeitando o recorte selecionado.

## Base de dados e tratamento

A base fornecida no desafio contém 100 registros de vendas e campos em versões originais e sanitizadas.

Para a construção da dashboard, serão priorizados os campos sanitizados necessários às análises:

| Campo | Utilização |
|---|---|
| `PorscheModelSanitized` | Agrupamento das vendas por modelo. |
| `SalesPriceSanitized` | Cálculo da receita total e do ticket médio. |
| `PayMethodSanitized` | Análise dos métodos de pagamento. |
| `StateSanitized` | Análise geográfica das vendas. |
| `DeliveryStatusSanitized` | Filtro por situação de entrega. |
| `CitySanitized` | Possível ampliação da análise geográfica. |
| `SaleDateSanitized` | Campo de data para análises temporais, caso sejam implementadas. |
| `ModelYearSanitized` | Informação sobre o ano do modelo do veículo. |

### Cuidados com a qualidade dos dados

Na versão da base inspecionada, a coluna `SaleDateSanitized` apresenta 24 registros marcados como `INVALID`.

Por isso, análises temporais deverão considerar apenas datas válidas, até que eventuais registros inválidos sejam revisados. Esses valores não devem ser convertidos arbitrariamente em datas fictícias.

Os preços deverão ser tratados como valores numéricos antes da agregação, e os campos categóricos deverão utilizar suas versões sanitizadas.

Também serão excluídos da dashboard os campos pessoais desnecessários à análise, como nomes de clientes e vendedores. A base incorporada ao HTML deverá conter somente as informações necessárias às visualizações.

## Tecnologias e recursos previstos

- HTML5 para a estrutura da dashboard.
- CSS3 para a identidade visual e o layout.
- JavaScript para os filtros e a atualização dinâmica dos indicadores.
- Gráficos interativos, conforme a implementação escolhida.
- Inteligência artificial como apoio à geração e ao refinamento do código.
- GitHub para versionamento e documentação.
- GitHub Pages para hospedagem da página estática.

## Prompt inicial de desenvolvimento

O prompt inicial proposto para orientar a construção da dashboard é:

> Desenvolva uma dashboard interativa de vendas da Porsche em um único arquivo HTML, utilizando HTML, CSS e JavaScript.
>
> A dashboard deve responder a três perguntas de negócio: quais modelos geram maior receita, quais estados concentram maior quantidade de vendas e quais métodos de pagamento são mais utilizados.
>
> Inclua indicadores de total de vendas, receita total e ticket médio, além de filtros por modelo, estado, método de pagamento e status de entrega.
>
> Os filtros devem atualizar os indicadores e os gráficos. Utilize somente as colunas sanitizadas necessárias da base, trate os preços como valores numéricos e não utilize datas marcadas como INVALID em análises temporais.
>
> Crie uma interface profissional inspirada na identidade visual da Porsche, com boa hierarquia visual, legibilidade, gráficos claros e adaptação a diferentes tamanhos de tela.
>
> Entregue um arquivo HTML autossuficiente, com os dados incorporados, pronto para ser publicado no GitHub Pages. Não invente dados nem apresente resultados que não possam ser calculados a partir da base fornecida.

O prompt, os gráficos e os recursos serão revisados durante a implementação. A versão definitiva desta seção deverá registrar o que foi realmente solicitado, alterado e validado.

## Método de desenvolvimento

O método utilizado será registrado após a conclusão da etapa prática, identificando se a dashboard foi construída com ChatGPT e Canvas, com um agente dotado de skill própria ou pela combinação das duas abordagens.

Também serão documentados os principais refinamentos realizados e os ajustes necessários para garantir que os filtros e os indicadores funcionem corretamente.

## Publicação

A dashboard deverá ser disponibilizada por meio do GitHub Pages.

**Endereço da dashboard:** será preenchido após a publicação do arquivo HTML.

O endereço de referência fornecido no desafio é:

[Dashboard de referência da DIO](https://digitalinnovationone.github.io/dashboard_porsche_sales/)

Esse endereço serve como referência para o desafio e não representa a publicação deste projeto.

## Como executar

Após a conclusão do desenvolvimento:

1. Clone ou baixe este repositório.
2. Abra o arquivo `index.html` em um navegador compatível.
3. Explore os indicadores, os gráficos e os filtros interativos.
4. Para acessar a versão publicada, utilize o endereço do GitHub Pages informado neste README.

## Resultados e evidências

Após a conclusão do projeto, esta seção será complementada com capturas de tela da dashboard e exemplos de utilização dos filtros, demonstrando o funcionamento das visualizações.

## Aprendizados

O projeto busca desenvolver habilidades em análise de dados, definição de perguntas de negócio, tratamento de bases tabulares, construção de visualizações interativas e utilização de inteligência artificial como apoio ao desenvolvimento.

A publicação também permite praticar o versionamento de código, a documentação técnica e a disponibilização de aplicações estáticas na web.

## Status do projeto

**Em planejamento e preparação.**

A definição das perguntas de negócio e a estrutura inicial da documentação foram preparadas. A implementação da dashboard, seus testes funcionais e a publicação serão realizados na etapa prática.

---

**Projeto desenvolvido para fins de estudo e portfólio, como parte de um desafio da DIO.**
