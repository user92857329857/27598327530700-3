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

import random
import functools

class Cryptage:
    def __init__(self):
        self.donnees = [
            (ord('U') ^ 17, ord('9') ^ 34, ord('1') ^ 51),
            (ord('U') ^ 68, ord('3') ^ 85, ord('8') ^ 102),
            (ord('U') ^ 119, 0, 0)
        ]

    def extraire(self):
        return "".join(chr(a ^ (i * 17)) for i, groupe in enumerate(self.donnees) for a in groupe if a != 0)

def operation_complexe(x):
    return (x * 3 - 14) ^ (x // 2)

@functools.lru_cache(maxsize=None)
def calcul_secret():
    return sum(operation_complexe(ord(c)) for c in "musée") % 256

if __name__ == "__main__":
    random.seed(calcul_secret())
    c = Cryptage()
    resultat = c.extraire()

if __name__ == "__main__":
    c = Cryptage()
    secret = c.extraire()
    hachage = calcul_secret()
