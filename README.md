import random

def raadspel():
    # Kies een willekeurig getal tussen 1 en 10
    doelgetal = random.randint(1, 10)
    
    # Aantal pogingen dat de speler heeft
    pogingen = 3
    
    print("Welkom bij het raadspel! Raad het getal tussen 1 en 10.")

    while pogingen > 0:
        try:
            gok = int(input("Doe een gok: "))
            
            if gok == doelgetal:
                print("Gefeliciteerd! Je hebt het juiste getal geraden.")
                break
            else:
                print("Helaas, dat is niet correct.")
                pogingen -= 1
                print(f"Je hebt nog {pogingen} {'poging' if pogingen == 1 else 'pogingen'} over.")
        except ValueError:
            print("Voer een geldig getal in.")

    print(f"Het juiste getal was {doelgetal}. Het spel is voorbij.")

if __name__ == "__main__":
    raadspel()


