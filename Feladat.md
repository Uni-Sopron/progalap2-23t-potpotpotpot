# Fun with flags

Készíts egy grafikus felülettel rendelkező programot, mely országok zászlóiról tart karban egy adatbázist, illetve statisztikákat képes bizonyos paramétereikről készíteni. 

## Kiinduló állapot
Adott egy [JSON fájl](flags.json), melyben az országokról található néhány alapvető információ, valamint egy [könyvtár](flags/), amiben az országok zászlajai találhatók SVG formátumban.

## Az elkészítendő alkalmazás funkciói

### Könyvtárválasztás
A program induláskor parancssori argumentumban várja, hogy melyik könyvtárban keresse a `flags` könyvtárat, és a `flags.json` fájlt.
Ha ez nincs megadva, dobjon fel egy ablakot, melyben kéri a felhasználót, hogy adjon meg egy elérési utat.
Ha a bármelyik módon megadott elérési út nem létezik, vagy a fenti konyvtár és fájl nem léteznek, akkor ismételje meg az előző lépést.

### Adattisztítás
Előfordulhatnak a JSON fájlban hiányos adatok, valamint olyan országok, melyekhez nincs zászló. Ezeket induláskor azonnal törölje a JSON fájlból.

### A felület felépítése
A lábbi funkciók több ablakba is szétszedhetők, de lehetnek egyben is. Nincs megkötés arra sem, miyen widgetek legyenek használva, csak a dunkciók legyenek elérhetők.
1. Látszódjon, hány ország van, és ezek közül hányhoz adottak szín információk 
2. Lehessen egy országot kiválasztani, és megadni, milyen színek fordulnak elő a zászlón. Ehhez jelenítse meg az ország zászlaját valahol.
3. Legyen lehetőség kétféle diagramm elkészítésére:
   1. `progress.png`: Egy bar-ploton mutatja kontinensenként, hogy hány országhoz vannak már meg a szín információk, és hányhoz nincsenek.
   2. `colors.png`: Két diagrammon ad információt a színinformációkkal már kiegészített zászlókról. Az elsőn színek szerint mutatja meg egy bar-ploton, hogy hány zászlón fordulnak elő. A mádodikon egy torta diagrammon mutatja meg, hogy az országok zászlajainak hány része 1, 2, 3, 4, stb. színű.
