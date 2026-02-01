# Crypto Price Scraper: Terra Luna V2

## Visão Geral do Projeto
Este projeto consiste em um script Python desenvolvido para realizar web scraping do preço atual da criptomoeda Terra Luna V2 (LUNA) diretamente do portal CoinMarketCap.com. A solução visa automatizar a coleta de dados de preços, carimbando-os com o timestamp da consulta e persistindo-os em uma estrutura de dados tabular (`pandas.DataFrame`), facilitando análises subsequentes.

## Problema de Negócio Solucionado
Em mercados de alta volatilidade como o de criptomoedas, o acesso rápido, preciso e consistente a dados de preços é fundamental para a tomada de decisões estratégicas de investimento e para a realização de análises de mercado aprofundadas. Este projeto automatiza o processo de aquisição do preço da Terra Luna V2, eliminando a necessidade de coleta manual. Tal automação permite que analistas de dados, investidores e outras partes interessadas obtenham e monitorem a cotação da criptomoeda de forma eficiente, integrando esses dados em seus modelos preditivos, dashboards de acompanhamento ou sistemas de trading.

## Principais Características para a Área de Negócio e Usuários
*   **Coleta Automatizada de Dados de Preço**: Reduz significativamente o esforço manual e o tempo despendido na busca por informações de preço, otimizando recursos e permitindo foco em atividades de maior valor agregado.
*   **Informações de Preço em Tempo (Quase) Real**: Fornece o preço mais atualizado da Terra Luna V2 no momento da execução, crucial para reações rápidas às dinâmicas do mercado.
*   **Base para Análise Preditiva e Decisões de Investimento**: Os dados coletados são estruturados em um formato `pandas.DataFrame`, ideal para integração com ferramentas de Business Intelligence (BI), construção de modelos de Machine Learning e execução de análises de risco e retorno.
*   **Flexibilidade e Adaptabilidade**: Embora focado inicialmente na Terra Luna V2, o script é modular e pode ser facilmente adaptado para monitorar outras criptomoedas ou ativos, bastando ajustar a URL de origem.
*   **Histórico de Dados Estruturado**: Com execuções periódicas, o projeto permite a construção de uma base histórica de preços, fundamental para identificar tendências de longo prazo, sazonalidades e padrões de comportamento do ativo.

## Tecnologias Utilizadas
*   **Python 3**: Linguagem de programação principal.
*   **`pandas`**: Biblioteca para manipulação e análise de dados, utilizada para estruturar e armazenar os preços coletados em DataFrames.
*   **`requests`**: Biblioteca HTTP para Python, empregada para realizar as requisições web e obter o conteúdo HTML das páginas do CoinMarketCap.
*   **`BeautifulSoup` (bs4)**: Biblioteca para parsing de HTML e XML, essencial para extrair os dados de preço de forma robusta do conteúdo web.
*   **`pytz`**: Biblioteca para trabalhar com fusos horários, garantindo a padronização e correção dos timestamps de consulta.
*   **`datetime`**: Módulo padrão do Python para manipulação de datas e horas.

## Configuração e Instalação
Para replicar e executar este projeto, é necessário ter o Python 3 instalado. As bibliotecas dependentes podem ser instaladas via `pip`:

```bash
pip install pandas requests beautifulsoup pytz time
