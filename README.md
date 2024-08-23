# Virtual-Stocks-Trading-Website
It is a virtual stock website with an account for users to register for, the ability to get quotes for shares of stocks and to virtually buy or sell them. The data which we receive is provided by the API of IEX cloud.

## USAGE
First, you will need to get an API key from IEX (free account registration), which lets you download stock quotes via their API (application programming interface) using URLs like https://cloud.iexapis.com/stable/stock/nflx/quote?token=API_KEY

With the API, run the following within a  IDE's terminal: $ export API_KEY=value (value is your acquired personal API KEY)

Start Flask’s built-in web server: $ flask run

## VIEWS
### Register

Allow a new user to register for an account, rendering an apology view if the form data is incomplete or if the username already exists in the database.
### Index

The homepage displays a table of the logged-in user's owned stocks, number of shares, current stock price, value of each holding. This view also shows the user's imaginary "cash" balance and the total of their "cash" plus stock value.
### Quote

Allows the user to submit a form to look up a stock's current price, retrieving real-time data from the IEX API. An error message is rendered if the stock symbol is invalid.
### Buy

Allows the user to "buy" stocks by submitting a form with the stock's symbol and number of shares. Checks to ensure the stock symbol is valid and the user can afford the purchase at the stock's current market price with their available balance, and stores the transaction history in the database.
### Sell

Allows the user to "sell" shares of any stock currently owned in their portfolio.
### History

Displays a table summarizing the user's past transactions (all buys and sells). Each row in the table lists whether the stock was bought or sold, the stock's symbol, the buy/sell price, the number of shares, and the transaction's date/time.
