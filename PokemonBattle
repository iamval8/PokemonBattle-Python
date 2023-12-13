import random

# Define Pokémon and their moves
pokemonMoves = {
    "Pikachu": ["Thunder Shock", "Quick Attack", "Tail Whip", "Growl"],
    "Charmander": ["Scratch", "Ember", "Growl", "Leer"],
    "Squirtle": ["Tackle", "Water Gun", "Tail Whip", "Withdraw"],
    "Bulbasaur": ["Tackle", "Vine Whip", "Growl", "Leech Seed"]
}

# Initial HP for each Pokémon
pokemonHp = {
    "Pikachu": 35,
    "Charmander": 39,
    "Squirtle": 44,
    "Bulbasaur": 45
}

# Player chooses Pokémon
print("Choose your Pokémon:")
for pokemon in pokemonMoves.keys():
    print(pokemon)
playerPokemon = input("Enter your Pokémon: ")
while playerPokemon not in pokemonMoves:
    print("Invalid choice. Please choose again.")
    playerPokemon = input("Enter your Pokémon: ")

# Opponent's Pokémon
opponentPokemon = random.choice(list(pokemonMoves.keys()))
while opponentPokemon == playerPokemon:
    opponentPokemon = random.choice(list(pokemonMoves.keys()))

print(f"You chose {playerPokemon}!")
print(f"Your opponent chose {opponentPokemon}!")

# Battle loop
while pokemonHp[playerPokemon] > 0 and pokemonHp[opponentPokemon] > 0:
    # Player's move choice
    print(f"Choose {playerPokemon}'s move:")
    for move in pokemonMoves[playerPokemon]:
        print(move)
    playerMove = input("Enter the move: ")
    while playerMove not in pokemonMoves[playerPokemon]:
        print("Invalid move. Please choose again.")
        playerMove = input("Enter the move: ")

    print(f"{playerPokemon} used {playerMove}!")

    # Opponent's move
    opponentMove = random.choice(pokemonMoves[opponentPokemon])
    print(f"{opponentPokemon} used {opponentMove}!")

    # Simulate damage
    pokemonHp[opponentPokemon] -= 10
    pokemonHp[playerPokemon] -= 10

    print(f"{playerPokemon} HP: {pokemonHp[playerPokemon]}")
    print(f"{opponentPokemon} HP: {pokemonHp[opponentPokemon]}")

# Determine and announce the winner
if pokemonHp[playerPokemon] > 0:
    print(f"{playerPokemon} wins!")
else:
    print(f"{opponentPokemon} wins!")
