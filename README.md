Blind Auction
Welcome to the Blind Auction, a Python-based command-line program that simulates a blind auction! In this project, participants can place bids anonymously, and the highest bidder is revealed at the end. It’s a fun way to practice dictionaries, loops, and user input handling in Python.

How It Works
The program starts by displaying a hammer ASCII art (via the art module) and a welcome message.
Users are prompted to enter their name and bid amount (in R$).
After each bid, the user decides whether to add another participant (yes or no).
The screen clears between entries to keep bids "blind" (simulated with 50 newlines).
Once all bids are entered, the program calculates and announces the winner with the highest bid.

Requirements
Python 3.x: Ensure Python is installed on your system.

Installation
Download or clone this repository to your computer.
Verify Python is installed by running python --version or python3 --version in your terminal.
Install the required art module (see above).
Run the program by opening a terminal in the project folder and typing:
python blind_auction_bid.py
