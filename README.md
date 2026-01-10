# Stock-portfolio-tracker
stock_prices = {
    "AAPL": 180,
    "TSLA": 250,
    "GOOGL": 135,
    "MSFT": 310
}

portfolio = {}
total = 0

print("Stock Portfolio Tracker")

while True:
    stock = input("Enter stock symbol or 'done': ").upper()
    if stock == "DONE":
        break
    if stock not in stock_prices:
        print("Stock not available")
        continue

    qty = int(input("Enter quantity: "))
    portfolio[stock] = qty
    total += stock_prices[stock] * qty

print("Portfolio Summary")
for s, q in portfolio.items():
    print(s, q, "shares")

print("Total Investment:", total)
