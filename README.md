# Blind Auction Project

## Description

This Python program simulates a blind auction. Participants enter their names and bids without knowing the bids of others. After everyone has placed their bids, the program determines and announces the winner based on the highest bid.

## How to Use

1.  **Run the script:** Execute the Python script. You will see a welcome message, an ASCII art hammer, and a separator line.
2.  **Enter your information:**
    * The program will ask "Please insert your name!". Type your name and press Enter.
    * Next, it will ask "Insert your bid! R$". Enter your bid amount as a whole number (integer) and press Enter.
3.  **Add more participants:**
    * The program will ask "Would you like to include another person? Type 'yes' or 'no'".
    * Type 'yes' if another person wants to bid and press Enter. The screen will clear (simulating a blind auction), and the program will prompt for the next participant's name and bid.
    * Type 'no' if there are no more participants and press Enter. The auction will conclude.
    * Typing anything other than 'yes' or 'no' will end the auction with an "Invalid input" message.
4.  **View the results:** Once all bids are collected, the program will announce the winner, stating their name and winning bid amount. It will also display a thank you message.

## Functionality

* **Participant Data Storage:** Uses a dictionary (`audiction_participation_list`) to store each participant's name as the key and their bid amount as the value.
* **Blind Bidding Simulation:** Clears the console screen (`print("\n" * 50)`) after each bid to prevent participants from seeing previous bids.
* **Multiple Participants:** Allows an unlimited number of participants to place bids until the user indicates no more participants.
* **Winner Determination:** Iterates through the stored bids to find the highest bid and the name of the participant who placed that bid.
* **Output:** Announces the winner and their winning bid.
* **ASCII Art:** Displays an ASCII art hammer at the beginning using the `art` module.

## Requirements

* Python 3.x
* `art` module (can be installed via pip: `pip install art`)

## Installation

1.  Ensure you have Python installed on your system.
2.  Install the `art` module if it's not already installed:
    ```bash
    pip install art
    ```
3.  Save the provided code as a `.py` file (e.g., `blind_auction.py`).
4.  Run the script using a Python interpreter:
    ```bash
    python blind_auction_bid.py
    ```

## Code Explanation

* **`import art`:** Imports the `art` module for the hammer ASCII art.
* **`print(art.hammer)`:** Prints the hammer art.
* **`print("Welcome to my blind auction project!\n______________________________________")`:** Prints the welcome message and separator.
* **`audiction_participation_list = {}`:** Initializes an empty dictionary to store participant names and their bids.
* **`audiction_is_roling = True`:** A boolean flag to control the main bidding loop.
* **`while audiction_is_roling:`:** The main loop that continues as long as there are participants willing to bid.
    * **`name = str(input("Please insert your name!\n"))`:** Prompts the current participant to enter their name.
    * **`price = int(input("Insert your bid!\nR$"))`:** Prompts the participant to enter their bid (as an integer).
    * **`audiction_participation_list[name] = price`:** Stores the participant's name and bid in the dictionary.
    * **`continue_the_bid = str(input("Would you like to include another person?\nType 'yes' or 'no'\n")).lower()`:** Asks if there are more bidders.
    * **`print("\n" * 50)`:** Clears the screen by printing 50 newline characters, simulating a blind auction.
    * **Conditional Logic:**
        * If `continue_the_bid` is "no", the bidding loop ends.
        * If `continue_the_bid` is "yes", the bidding loop continues.
        * For any other input, an "Invalid input" message is printed, and the loop ends.
* **Winner Determination:**
    * **`winner = ""`:** Initializes an empty string to store the winner's name.
    * **`max_bid = 0`:** Initializes a variable to keep track of the highest bid.
    * **`for bidder in audiction_participation_list:`:** Iterates through each participant's name (key) in the `audiction_participation_list`.
        * **`bid_ammount = audiction_participation_list[bidder]`:** Retrieves the bid amount for the current bidder.
        * **`if bid_ammount > max_bid:`:** Checks if the current bid is higher than the current `max_bid`.
            * If it is, the `max_bid` is updated, and the `winner`'s name is set to the current `bidder`.
* **Result Announcement:**
    * **`print(f"The winner is {winner}! With the bid of R${max_bid}!\nThanks for testing my project! :)")`:** Prints the name of the winner and their winning bid.
