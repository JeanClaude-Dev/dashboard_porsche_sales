# Porsche Sales Intelligence

Dashboard interativa de vendas Porsche em um único arquivo HTML, preparada para GitHub Pages. A [dashboard](./index.html) reúne os dados sanitizados e a foto de fundo no próprio arquivo: não depende de bibliotecas, serviços externos nem de outros arquivos do projeto.

## Perguntas de negócio

1. **Quais modelos geram mais receita?** O ranking por faturamento ajuda a identificar onde a receita está concentrada, além de comparar somente o número de unidades.
2. **Em quais cidades vendemos mais?** O volume por cidade ajuda a explorar a distribuição geográfica; os filtros de estado e cidade permitem analisar cada região.
3. **Como os clientes pagam?** A participação dos métodos de pagamento ajuda a entender a composição das vendas por modalidade.

Os indicadores no topo mostram quantidade de vendas, receita, ticket médio e modelo mais vendido por unidades. Os filtros de modelo, ano do modelo, estado, cidade e pagamento atualizam todos os indicadores e gráficos.

## Dados e tratamento

- A fonte foi a planilha sanitizada fornecida com o desafio. Ela foi usada localmente para montar os dados da dashboard, mas não foi incluída no repositório, pois contém campos pessoais que não são necessários à análise.
- Foram utilizados somente os campos sanitizados de modelo, ano do modelo, preço, método de pagamento, cidade e estado. Nomes de clientes e vendedores, datas e quilometragem não foram incorporados ao HTML.
- Os preços sanitizados foram convertidos para números decimais, e os anos do modelo para números inteiros; os anos são usados como filtro categórico na interface.
- Os 100 registros possuem os seis campos selecionados preenchidos. A receita total é **US$ 12.827.800,50** e o ticket médio é **US$ 128.278,01**.
- O repositório contém apenas os dois arquivos necessários ao projeto: `index.html` e `README.md`. A planilha de origem e os arquivos de exemplo não foram enviados.

## Perguntas e especificação usada

**Síntese da especificação que orientou a implementação** (não é uma transcrição de uma sessão do ChatGPT Canvas):

> Crie uma dashboard executiva de vendas Porsche em um único arquivo HTML, em português, usando somente as colunas sanitizadas da planilha. Responda a três perguntas: quais modelos geram mais receita, em quais cidades há mais vendas e como os clientes pagam. Inclua filtros para modelo, ano do modelo, estado, cidade e método de pagamento; indicadores para quantidade de vendas, receita, ticket médio e modelo líder; e gráficos atualizados por todos os filtros. Use um visual escuro e sofisticado, com vermelho e dourado, responsivo para celular e sem dependências externas. Não inclua nomes de clientes ou vendedores.

O escopo foi refinado para combinar perguntas complementares de receita, distribuição geográfica e pagamento. O ranking de modelos passou a destacar receita, além do volume de vendas; os filtros foram aplicados a todos os indicadores e gráficos; e a imagem ilustrativa foi incorporada ao HTML para manter o arquivo autônomo.

## Ferramenta

O desenvolvimento foi feito com assistência de IA no VS Code. Não foi utilizado ChatGPT Canvas nem um agente próprio com skill. O exemplo fornecido serviu de referência visual, e a implementação final foi construída e validada localmente.

## Publicação

- **Repositório público:** https://github.com/JeanClaude-Dev/dashboard_Porsche_Sales
- **Dashboard publicada:** https://jeanclaude-dev.github.io/dashboard_Porsche_Sales/
- **Status:** publicação conferida no GitHub Pages; a página abre com os 100 registros e os filtros atualizam os indicadores e gráficos.

O Pages publica a partir da branch `main` e da pasta raiz (`/(root)`).

## Conferência antes da entrega

- [x] Três perguntas de negócio, indicadores de topo e filtros interativos.
- [x] `index.html` em arquivo único, sem dependências externas; dados pessoais excluídos.
- [x] Repositório público com somente `index.html` e `README.md`.
- [x] GitHub Pages ativo; endereço publicado e filtros conferidos.
- [x] Link do repositório informado como entrega.

**Ajuste recomendado:** o nome atual `dashboard_Porsche_Sales` é legível e sem acentos, mas contém maiúsculas e underscores. Para seguir literalmente a recomendação de usar minúsculas, renomeie-o para `dashboard-porsche-sales`; a URL do Pages também mudará.
