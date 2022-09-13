# Historical Market Data

Collection of crypto data (klines) from various centralized exchanges for creating a comparison table of crypto pairs trade volume.

## Starting up (locally)

Requirements:

* python, pip, jupyter notebook (any other working environment)

Instruction:

* create and activate a virtualenv

* open notebook in browser

## Working notebook

To extract klines from CEX needs to use an REST API. Each exchange has its own request procedure (see for Public Endpoints--> Market Data)

* import the required libraries and packeges

* create the variables:
 `date_to`,
 `period`

* create a lists of CEXes and Pairs for work with (checking score on the CoinMarketCap)

* create a functions to get data from exchanges:

* `def fetch_cex_daily_data(pair, date_to, period, extended = False)`
* cross-check output data with market data on CoinGecko, CoinMarketCap, and on the exchange itself

* create a function to formate outputs:
`def get_data_formated(data, pair)`

* create a function for klines by exchange pair:
`def get_klines_by_exchange_pair(exchange, pair, date_to, period, extended = False)`

* create a dictionary of klines by exchange:
`def get_klines(exchanges, pairs, date_to, period, extended = False)`

* save klines dictionary as CSV files:
`def save_klines_dic_as_csv(klines)`

* create a final DataFrames from list of CSV files:
`def create_list_of_dataframes(csv_files)`
