 # Crypto Price Scraper: Terra Luna V2

# Visão Geral
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
Como Executar
Abra o Notebook Jupyter/Colab: Carregue o arquivo .ipynb fornecido em um ambiente Jupyter ou Google Colab.
Execute as Células em Sequência: Execute cada célula de código no notebook de cima para baixo. O notebook está estruturado para:
Importar as bibliotecas necessárias.
Definir a URL alvo e os cabeçalhos da requisição.
Buscar o conteúdo da página web.
Fazer o parsing do HTML e extrair o preço da Terra Luna V2.
Formatar o preço e o carimbo de data/hora.
Criar e atualizar um DataFrame do pandas com o preço e o carimbo de data/hora mais recentes.
Estrutura do Projeto (Células do Notebook)
Importações: Carrega pandas, requests, bs4, time, pytz, datetime.
Configuração de Hora: Inicializa o fuso horário 'America/Sao_Paulo' e captura o carimbo de data/hora atual.
URL e Headers: Define a URL do CoinMarketCap para Terra Luna V2 e configura os cabeçalhos HTTP para evitar bloqueios.
Web Scraping: Usa requests para obter a página e BeautifulSoup para fazer o parsing. Nota: O objeto soup precisa ser criado a partir de response.content antes de extrair o preço.
Data Extração e Limpeza: Extrai a string do preço, limpa-a removendo símbolos de moeda e vírgulas, e a converte para float.
Operações de DataFrame: Cria um dicionário com os dados extraídos e os anexa a um DataFrame do pandas.
Exemplo de Saída de Dados (DataFrame)
Moeda	Hora Consulta	Preço
Luna	2026-02-01 01:08:57	0.3561
...	...	...
Esta tabela mostra um exemplo dos dados coletados, com a criptomoeda, o carimbo de data/hora da consulta e seu preço.

Melhorias Futuras
Implementar tratamento de erros para web scraping (por exemplo, se a estrutura do site mudar ou a requisição falhar).
Agendar o script para rodar em intervalos regulares para coleta contínua de dados.
Armazenar dados persistentemente em um arquivo CSV, banco de dados ou armazenamento em nuvem.
Visualizar tendências de preços ao longo do tempo.
Monitorar múltiplas criptomoedas.
Crypto Price Scraper: Terra Luna V2 (English Version)
Overview
This project is a simple Python script designed to scrape the current price of Terra Luna V2 (LUNA) from CoinMarketCap.com. It uses web scraping techniques to extract the cryptocurrency's price, timestamps the data, and stores it in a pandas DataFrame.

Business Problem it Solves
In the volatile cryptocurrency market, investment decisions and market analysis require quick and consistent access to price data. This project solves the problem of manually obtaining the price of a specific cryptocurrency (Terra Luna V2) by automating data collection, making it easily accessible and analyzable. This allows users and businesses to effortlessly track the quote, integrating it into monitoring processes or investment strategies.

Key Business/User Characteristics
Automated Price Collection: Eliminates the need for manual monitoring, saving time and ensuring data consistency.
Near Real-time Price Data: Provides the updated price of Terra Luna V2 at the time of query, crucial for rapid market analysis.
Foundation for Analysis and Decision Making: Data is stored in a structured format (pandas DataFrame), facilitating further analysis, visualizations, and integration with other business intelligence tools.
Specific Asset Monitoring: Focused on Terra Luna V2, but easily adaptable to monitor other cryptocurrencies relevant to your portfolio or business strategy.
Historical Record: When run periodically, the script creates a historical price record, allowing for the identification of trends and patterns over time.
Technologies Used
Python 3
pandas: For data manipulation and storage in DataFrames.
requests: For making HTTP requests to fetch web page content.
BeautifulSoup4 (bs4): For parsing HTML and extracting data from web pages.
pytz: For handling timezones.
datetime: For working with dates and times.
Setup and Installation
To run this project, you need to have Python 3 installed. You can install the required libraries using pip:

pip install pandas requests beautifulsoup4 pytz
How to Run
Open the Jupyter/Colab Notebook: Load the provided .ipynb file in a Jupyter environment or Google Colab.
Execute Cells Sequentially: Run each code cell in the notebook from top to bottom. The notebook is structured to:
Import necessary libraries.
Define the target URL and request headers.
Fetch the webpage content.
Parse the HTML and extract the Terra Luna V2 price.
Format the price and timestamp.
Create and update a pandas DataFrame with the latest price and timestamp.
Project Structure (Notebook Cells)
Imports: Loads pandas, requests, bs4, time, pytz, datetime.
Time Setup: Initializes the 'America/Sao_Paulo' timezone and captures the current timestamp.
URL and Headers: Defines the CoinMarketCap URL for Terra Luna V2 and sets HTTP headers to prevent blocking.
Web Scraping: Uses requests to get the page and BeautifulSoup to parse it. Note: The soup object needs to be created from response.content before extracting the price.
Data Extraction & Cleaning: Extracts the price string, cleans it by removing currency symbols and commas, and converts it to a float.
DataFrame Operations: Creates a dictionary with the extracted data and appends it to a pandas DataFrame.
Example Data Output (DataFrame)
Moeda	Hora Consulta	Preço
Luna	2026-02-01 01:08:57	0.3561
...	...	...
This table shows an example of the data collected, with the cryptocurrency, the timestamp of the consultation, and its price.

Future Enhancements
Implement error handling for web scraping (e.g., if the website structure changes or the request fails).
Schedule the script to run at regular intervals for continuous data collection.
Store data persistently in a CSV file, database, or cloud storage.
Visualize price trends over time.
Track multiple cryptocurrencies.
