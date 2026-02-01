#  Crypto Price Scraper: Terra Luna V2

## Visão Geral
Este projeto é um script Python simples projetado para coletar o preço atual do Terra Luna V2 (LUNA) do CoinMarketCap.com. Ele utiliza técnicas de web scraping para extrair o preço da criptomoeda, carimba os dados com o tempo e os armazena em um DataFrame do pandas.

## Problema de Negócio que Soluciona
No cenário volátil do mercado de criptomoedas, a tomada de decisões de investimento ou a análise de mercado requerem acesso rápido e consistente a dados de preços. Este projeto soluciona o problema de obter manualmente o preço de uma criptomoeda específica (Terra Luna V2), automatizando a coleta desses dados para que sejam facilmente acessíveis e analisáveis. Isso permite que usuários e empresas acompanhem a cotação sem esforço, integrando-a em processos de monitoramento ou estratégias de investimento.

## Principais Características para Negócio/Usuário
-   **Coleta Automatizada de Preços**: Elimina a necessidade de monitoramento manual, economizando tempo e garantindo a consistência dos dados.
-   **Dados de Preço em Tempo Quase Real**: Fornece o preço atualizado da Terra Luna V2 no momento da consulta, crucial para análises de mercado rápidas.
-   **Base para Análise e Tomada de Decisão**: Os dados são armazenados em um formato estruturado (DataFrame do pandas), facilitando análises posteriores, visualizações e a integração com outras ferramentas de business intelligence.
-   **Monitoramento de Ativos Específicos**: Focado na Terra Luna V2, mas facilmente adaptável para monitorar outras criptomoedas relevantes para o seu portfólio ou estratégia de negócio.
-   **Registro Histórico**: Ao ser executado periodicamente, o script cria um registro histórico de preços, permitindo a identificação de tendências e padrões ao longo do tempo.

## Tecnologias Utilizadas
-   Python 3
-   `pandas`: Para manipulação e armazenamento de dados em DataFrames.
-   `requests`: Para fazer requisições HTTP e obter o conteúdo das páginas web.
-   `BeautifulSoup4` (bs4): Para fazer o parsing do HTML e extrair dados das páginas web.
-   `pytz`: Para lidar com fusos horários.
-   `datetime`: Para trabalhar com datas e horas.

## Configuração e Instalação
Para rodar este projeto, você precisa ter o Python 3 instalado. Você pode instalar as bibliotecas necessárias usando `pip`:

```bash
pip install pandas requests beautifulsoup pytz
