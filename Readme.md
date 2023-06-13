                           # HANGMAN GAME

![HangMan Image](/screenshots/hangman.jpg)

## Import required packages and files;

![HangMan Image](/screenshots/import_packages.PNG)

## Choose a random word from a word_list and add number of life :

'''Python
chosen_word = random.choice(word_list)
word_length = len(chosen_word)

end_of_game = False
lives = 6

'''

## Create blanks and guess the blanks:

'''Python
display = []
for _ in range(word_length):
display += "_"

while not end_of_game:
guess = input("Guess a letter: ").lower()

    if guess in display:
        print(f"You've already guessed {guess}")

'''

## Check guessed letter:

''' Python
for position in range(word_length):
letter = chosen_word[position] # print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
if letter==guess:
display[position] = letter
'''

## Check if user is wrong.

'''Python
if guess not in chosen_word:

        print(f"You guessed {guess}, that's not in the word. You lose a life.")

        lives -= 1
        if lives==0:
            end_of_game = True
            print("You lose.")
    print(f"{' '.join(display)}")

'''

## Check if user has got all letters.

'''Python
if "\_" not in display:
end_of_game = True
print("You win.")

    from hangman_art import stages

    print(stages[lives])

'''
![screen1](/screenshots/screen1.JPG)

![screen1](/screenshots/last%20screen.JPG)
