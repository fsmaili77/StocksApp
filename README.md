# Stock Market Tracker
This is a simple web application built with ASP.NET Core and Razor Pages that allows users to view real-time stock market information. The application fetches stock data from the Finnhub API and displays the current, highest, lowest, and opening prices for a selected stock symbol.

## Features
- **Real-Time Stock Data:** The application retrieves real-time stock quotes, including the current price, high price, low price, and opening price for the day.
- **Configurable Default Stock:** The default stock symbol displayed on the homepage can be configured in the application's settings. If not specified, the app defaults to displaying Microsoft's stock (MSFT).
- **Responsive UI:** The application's user interface is designed using Razor Pages and HTML/CSS, ensuring a clean and responsive layout.

## Project Structure
`Program.cs`: Configures the services and middleware used in the application, including setting up dependency injection for the FinnhubService and reading configuration settings.

`HomeController.cs`: Handles the logic for fetching stock data from the Finnhub API using the FinnhubService and passing it to the view. The controller also ensures that a default stock symbol is used if none is specified.

`FinnhubService.cs`: Encapsulates the logic for communicating with the Finnhub API. It sends HTTP requests to retrieve stock data and processes the JSON response.

`Stock.cs`: A simple model class representing the stock data, including the stock symbol, current price, highest price, lowest price, and opening price.

`Index.cshtml`: The Razor view that displays the stock data in a user-friendly format. The view is styled with basic HTML and CSS.

## Configuration
Before running the application, ensure you have set up the following configurations:

1. **Finnhub API Token:** You'll need a valid API token from Finnhub. Add this token to your appsettings.json or environment variables under the key FinnhubToken.
2. **Default Stock Symbol:** You can set a default stock symbol in your configuration file under the TradingOptions section. If not set, the application defaults to MSFT.


## How to Run
1. Clone the repository to your local machine.
2. Open the solution in Visual Studio or your preferred IDE.
3. Add your Finnhub API token to the configuration.
4. Build and run the application.

## Dependencies
- .NET 6.0 or later
- ASP.NET Core
- Finnhub API
## Future Enhancements
- Add support for multiple stock symbols.
- Implement charting to visualize stock trends.
- Add personalized stock watchlists.

