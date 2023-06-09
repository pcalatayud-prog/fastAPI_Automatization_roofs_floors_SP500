# Yahoo Stock Technical Analysis API

This repository contains scripts and data files used to create an API for generating technical analysis data and images for S&P 500 stocks. The API uses FastAPI to display plots of each stock's floors and roofs, as determined by an automated technical analysis routine.

## Files and Directories

* `intersection`: folder with the current values of the floors and roofs for each stock in CSV format for each ticker.
* `main.py`: Python script that creates the API and serves the images at the IP/ticker/{ticker} endpoint.
* `pictures_analysis`: `{ticker}.png` photos after applying the "our technical routine" to create the floors and roofs.
* `pivot_log.py`: Python script with all the functions used to create the floors and roofs.
* `sp_500_Stocks.csv`: CSV file with the 500 tickers of the S&P 500 index. Note that this file may not be up-to-date.
* `Calculate_all_sp500_floors_and_roofs.py`: Python script that generates the automatic technical analysis and images for each ticker in the `pictures_analysis` folder.
* `yahoo-single.py`: Python script that generates images for a single ticker, which can be selected inside the script.
* `versions.py`: Library versions.

## Running the API

To run the API locally, navigate to the directory and execute the `main.py` script. This will create a local API that can be accessed in a web browser or through programmatic API calls. The API will generate images for each stock in the `sp_500_Stocks.csv` file and serve them at the `IP/ticker/{ticker}` endpoint.

Please note that in order to run the API locally, the `main.py` script must be executed from within the `/home/sharing/yahoo` directory. A more permanent solution may involve adding the command to the `.bashrc` file.

## Example Visualization

![Alt text](example.png "Example of Visualization")

This image shows an example of the visualization that can be generated using the scripts and data in this repository. The visualization includes the floors and roofs for a single stock, as well as other technical analysis data. By using the API, these visualizations can be generated for any stock in the S&P 500 index.

## Conclusion

The aim of this repo is to create an automated technical analysis in daily historical data for the S&P 500 stock tickers, as well as visualizations through FastAPI. The technical analysis is created automatically, so its accuracy may not be the best.
