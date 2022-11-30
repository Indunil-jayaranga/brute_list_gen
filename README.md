# brute_list_gen


print("   _                _           _ _     _                        ")
print("  | |__  _ __ _   _| |_ ___    | (_)___| |_      __ _  ___ _ __  ")
print("  | '_ \| '__| | | | __/ _ \   | | / __| __|    / _` |/ _ \ '_ \ ")
print("  | |_) | |  | |_| | ||  __/   | | \__ \ |_    | (_| |  __/ | | |")
print("  |_.__/|_|   \__,_|\__\___|___|_|_|___/\__|____\__, |\___|_| |_|")
print("                          |_____|         |_____|___/                               ")
print("------------------------------------------------------------V-0.1----")


with open("output.txt",'w') as file:

  guessings = []
  capital = []

  while True:
    guesses = str(input("Input Guesses\t:"))
    guessings.append(guesses)
    if not guesses:
      break 

  def brute(guess_list):
    for main_item in guess_list:
      for item in guess_list: 
        file.write(main_item+item + '\n')
        file.write(main_item+'@'+item+ '\n')
        file.write(main_item+'@#'+item+ '\n')
        file.write(main_item+'#@'+item+ '\n')

  first_capital = [i.capitalize() for i in guessings]
  capital_all = [i.upper() for i in guessings]
  
  brute(first_capital)
  brute(guessings)
