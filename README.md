- 👋 Hi, I’m @Mohamedlaminedev
- 👀 I’m interested in Computer science in general
- 🌱 I’m currently learning java web design and computer organizatio 
- 💞️ I’m looking to collaborate on .
- 📫 How to reach me ...

<!---
Mohamedlaminedev/Mohamedlaminedev is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
def load_game():
    """
    Populate the game dictionary by iterating over lines in game.txt.
    Each line is split by tab, and the first value is cast to integer as the key.
    The corresponding values are added to a list associated with the key.
    """
    game = {}
    with open('game.txt', 'r') as file:
        for line in file:
            values = line.strip().split('\t')
            key = int(values[0])
            game[key] = values[1:]
    return game

def load_objects():
    """
    Populate the objects dictionary by iterating over lines in object.txt.
    Each line is split by tab, and the first two values are cast to integers for the key.
    The rest of the values in the line are added to a list associated with the key.
    """
    objects = {}
    with open('object.txt', 'r') as file:
        for line in file:
            values = line.strip().split('\t')
            key = (int(values[0]), int(values[1]), values[2])
            objects[key] = values[3:]
    return objects

def load_travel_table():
    """
    Populate the travel dictionary by iterating over lines in travel.txt.
    Each line is split by tab, and the first two values are cast to integers for the key.
    The third value is associated with the key in the dictionary.
    """
    travel = {}
    with open('travel.txt', 'r') as file:
        for line in file:
            values = line.strip().split('\t')
            key = (int(values[0]), int(values[1]))
            travel[key] = values[2]
    return travel

def print_instructions():
    """
    Open instructions.txt in read mode and print its contents.
    """
    with open('instructions.txt', 'r') as file:
        print(file.read())

# You can call these functions as needed in your adventure game.
