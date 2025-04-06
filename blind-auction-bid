import art

print(art.hammer)
print("Welcome to my blind auction project!\n______________________________________")

audiction_participation_list = {}

audiction_is_roling = True
while audiction_is_roling:
    name = str(input("Please insert your name!\n"))
    price = int(input("Insert your bid!\nR$"))
    audiction_participation_list[name] = price
    continue_the_bid = str(input("Would you like to include another person?\nType 'yes' or 'no'\n")).lower()
    print("\n" * 50)
    if continue_the_bid == "no":
        print("Thanks for using my auction project! :)")
        audiction_is_roling = False
    elif continue_the_bid == "yes":
        audiction_is_roling = True
    else:
        print("Invalid input. End of the program.")
        audiction_is_roling = False

winner = ""
max_bid = 0
for bidder in audiction_participation_list:
    bid_ammount = audiction_participation_list[bidder]
    if bid_ammount > max_bid:
        max_bid = bid_ammount
        winner = bidder

print(f"The winner is {winner}! With the bid of R${max_bid}!\nThanks for testing my project! :)")
