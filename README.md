# Crypto Signals

Crypto Signals is automates your crpyto currency Technical Analysis (TA) and trading.

Track over 500 coins across Bittrex, Bitfinex, GDAX, Gemini and more!

Technical Analysis Automated:
* Relative Strength Index (RSI)
* Ichimoku Cloud (Leading Span A, Leading Span B, Conversion Line, Base Line)
* Simple Moving Average
* Exponential Moving Average
* Breakouts / Pumps

Alerts:
* SMS via Twilio
* Email
* Slack

Features:
* Modular code for easy trading strategy implementation
* Easy install with Docker

You can build on top of this tool and implement algorithm trading and some machine learning models to experiment with predictive analysis.

Coming Soon:
* Automtated buying/selling
* MACD
* Bollinger Band
* Web Client :)


Shoutouts:
* To Bittrex for an awesome API
* Eric Somdahl for writing the Python wrapper for the Bittrex API
* Ryan Mullin for implementing the getHistoricalData() method on v2 of the Bittrex API

# How to use (Docker)
* First make sure you have [Docker installed](https://docs.docker.com/engine/installation/)
* Next, to create the docker image run `make build` in the root of the project directory.
* Once built copy template.env to .env and add your API keys, at a minimum read-only Bittrex keys are required.
* Make sure to also update the market\_pairs settings within the .env with comma seperated market pair values that match Bittrex's format (i.e. ETH/BTC)

## How to run
In the root directory run `docker-compose run app` or `make run` if you don't have docker-compose.

# How to use (Local)
To install the dependencies for this project, run "pip install -r requirements.txt" in the app directory.
Add a secrets.json file to the app directory of your project.
The contents of the file should mirror the following:

```json
{
    "exchanges": {
        "bittrex": {
            "required": {
                "key": "BITTREX_API_KEY",
                "secret": "BITTREX_SECRET"
            }
        }
    }
}
```

For other available options see the app/default-config.json directory.

## How to run
Navigate to the app directory in your terminal and run with "python app.py"

# Liability
I am not your financial adviser, nor is this tool. Use this program as an educational tool, and nothing more. None of the contributors to this project are liable for any loses you may incur. Be wise and always do your own research.
