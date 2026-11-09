# Porsche Sales Intelligence

Dashboard interativa de vendas Porsche, feita em HTML único e pronta para publicação no GitHub Pages. O arquivo [index.html](./index.html) funciona sem bibliotecas ou chamadas externas: os dados e a foto do banner estão incorporados no próprio HTML. A foto foi incorporada a partir do arquivo `image_porsche.jpg` fornecido na pasta de exemplos.

## Perguntas de negócio

1. **Quais modelos geram mais receita?** O ranking por receita ajuda a identificar onde o faturamento está concentrado, em vez de olhar apenas o número de unidades.
2. **Em quais cidades vendemos mais?** O ranking de vendas por cidade, combinado com os filtros de estado e cidade, ajuda a explorar a distribuição geográfica.
3. **Como os clientes pagam?** A distribuição por método de pagamento mostra o peso de cada modalidade no volume de vendas.

Os indicadores no topo mostram vendas filtradas, receita, ticket médio e modelo mais vendido por quantidade. Os filtros de modelo, ano do modelo, estado, cidade e método de pagamento atualizam os indicadores e os três gráficos simultaneamente.

## Dados e tratamento

- A fonte usada foi a planilha `8683bed0-cc33-4e06-bca9-04db9c31f9e2.xlsx`, fornecida na pasta `data/` junto ao desafio, que já contém colunas sanitizadas.
- A dashboard usa `PorscheModelSanitized`, `ModelYearSanitized`, `SalesPriceSanitized`, `PayMethodSanitized`, `CitySanitized` e `StateSanitized`.
- O preço é convertido para número durante a leitura da base; o ano do modelo é tratado como categoria para os filtros.
- Nomes de clientes e vendedores, datas, quilometragem e demais campos que não respondem às perguntas escolhidas não são incorporados ao HTML.
- Os 100 registros têm modelo, ano, preço, pagamento, cidade e estado preenchidos nas colunas sanitizadas. Os preços totalizam **US$ 12.827.800,50**, com ticket médio de **US$ 128.278,01**.
- A planilha permanece na pasta `data/` como fonte local e não foi copiada para dentro do HTML. Antes de publicar o repositório, não inclua a planilha original: ela contém campos pessoais que não são necessários à análise.

## Prompt e refinamento

**Síntese do prompt de especificação da versão final** (registrada para documentar o escopo; não foi feita uma sessão separada no Canvas):

> Crie uma dashboard executiva em um único arquivo HTML, em português, a partir das colunas sanitizadas da planilha de vendas Porsche. Responda: quais modelos geram mais receita, em quais cidades há mais vendas e qual é a distribuição por método de pagamento. Inclua filtros interativos para modelo, ano do modelo, estado, cidade e pagamento; indicadores para vendas, receita, ticket médio e modelo líder; e gráficos que sejam recalculados por todos os filtros. Use um visual escuro e sofisticado, com vermelho e dourado como acentos, responsivo para celular e sem dependências externas. Não inclua nomes de clientes ou vendedores.

Durante a implementação, o escopo foi definido para priorizar três perguntas complementares — receita, presença geográfica e pagamento — em vez de acumular gráficos sem uma decisão associada. O ranking de modelos foi ordenado por receita (não só por unidades), a análise de localização usa vendas por cidade e os filtros atuam em todos os indicadores e gráficos. A implementação usa HTML, CSS e JavaScript nativos para manter o artefato em arquivo único.

## Ferramenta

O desenvolvimento foi feito com assistência de IA no VS Code, usando os arquivos do desafio e o exemplo visual como referência. Não foi usado ChatGPT Canvas nem um agente próprio com skill.

## Publicação

**Dashboard:** https://jeanclaude-dev.github.io/dashboard_Porsche_Sales/

O repositório contém apenas os dois arquivos necessários para este desafio: `index.html` e `README.md`. Para ativar o GitHub Pages, selecione a branch principal e a pasta raiz em **Settings → Pages**, caso a publicação ainda não esteja ativa.
