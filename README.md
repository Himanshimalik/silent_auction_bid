# silent_auction_bid
A program to aid silent auction bidding. This kind of bidding is usually done for government bonds and other such official auctions to decide the highest bidder when the bidding is complete.
<br>
from replit import clear
from art import logo
<br>

print(logo)
bid = {}

name = input("What is your name?\n")
bid_amount = int(input("Whats your bid amount?\n$"))

bid[name] = bid_amount
more_bids = str.lower(input("Do you have any other bidders?\nYes or No?"))

while more_bids == "yes":
    clear()
    name = input("What is your name?\n")
    bid_amount = int(input("Whats your bid amount?\n$"))
    bid[name] = bid_amount
    more_bids = str.lower(input("Do you have any other bidders?\nYes or No?"))

print(max(bid))
highest_bid = max(bid)

print(f"The highest bidder is {max(bid)} with ${bid[highest_bid]} being the highest bid.")
