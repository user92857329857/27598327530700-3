message = """
🎉 Félicitations, cher(e) participant(e) ! 🎉

Vous voilà enfin sorti(e) du **musée de H**. Une épreuve de plus derrière vous, un pas de plus vers l'inconnu...  
N'est-ce pas une sensation exaltante ? Un instant que l'on aimerait savourer encore et encore, mais hélas, le **temps nous est compté**.  

## 🌀 Un tournant décisif  
Vous l’avez sans doute déjà pressenti : les épreuves ont pris une toute nouvelle tournure.  
🔎 **Fini les recherches.**  
💡 **Place à l’imagination.**  

Désormais, il ne s’agit plus de simplement chercher… **Il faut créer, il faut inventer, il faut oser.**  

## 🚪 Vers l'Épreuve 3  
Votre prochain défi ne s’ouvrira pas avec une simple clé.  
Il faudra faire preuve de **perspicacité**, d’**intuition**, et surtout, d’**audace**.  

Oserez-vous franchir cette nouvelle frontière ?  

Bonne chance. Vous en aurez besoin.  

---

📌 *Les véritables joueurs ne se distinguent pas par ce qu'ils trouvent, mais par ce qu'ils imaginent...*
"""

#class Cryptage:
    def __init__(self):
        self.donnees = [
            (101, 91, 66),
            (49, 102, 66),
            (34, 0, 0)
        ]

    def extraire(self):
        return "".join(chr(val ^ (i * 17)) for i, group in enumerate(self.donnees) for val in group if val != 0)

def calcul_secret():
    valeurs = [17, 34, 51, 68, 85, 102, 119]
    return sum(x**2 for x in valeurs) % 256

if __name__ == "__main__":
    c = Cryptage()
    secret = c.extraire()
    hachage = calcul_secret()
