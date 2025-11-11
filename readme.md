# Gridek használata

## Alapbeállítások

**box-sizing:border-box** - _minden elemre alkalmazza, hogy  apadding és a border beleszámítson a teljes szálességbe/magasságba. Könnyebb a dobozok méretezése_

**img:width:100%** - _a képek mindig kitöltik a szülőelem szélességét, arányosan méretezve_ 

## NAV (navigáció)

**list-style: none** - _nincs listajel_

**display:grid;** - _grid elrendezése a menüpontokhoz_

**grid-auto-flow:collumn** - _a menüpontok egymás mellé kerülnek_

**justify-content:center** - _középre igazítás vízszintesen_

**align-items:center** - _középre igazítás függőlegesen_

**gap:2rem** - _2rem távolság a menüpontok között_

**padding:10px** - _belső margó a listán belül_

## Reszponzív menü (600px alatt)

**@media(max-width:600px){nav ul{grid-auto-flow:row;justify-items: center; gap: 1rem;}}** - _kis képernyőn a menü pontok egymás alá kerülnek, középre igazítva, kisebb térközzel.

## Tartalomdobozok kezdőlap (article+.cikk)

**display:grid** - _grid elrendezés a cikkekhez_

**grid-template-columns: repeat(auto-fit, minmax(200px, 1fr))** - _annyi oszlopot hoz létre, amennyi elfér, minimum 200px szélességgel_

**gap: 10px** - _távolság a cikkek között_

**padding: 10px** - _belső margó a gridben_

**text-align: center** - _a szöveg középre igazítva_

**padding: 10px** - _belső margó_

**box-sizing: border-box** - _padding és border beleszámít a méretbe_

**display: grid** _grid elrendezés a cikken belül_

**grid-template-rows: 50px 1fr auto** - _három sor: felső 50px (pl. cím), középső rugalmas, alsó automatikus_

**.cikk div { overflow: hidden; }** - _A cikken belüli kilógó tartalom elrejtve._

## sorrend módosítása

**.cikk:nth-child(3) { order: -1; }** - _a sorrendet cseréljük fel_

## Reszponzív tartalomdobozok

**@media (min-width: 800px) { article { grid-template-columns: repeat(3, 1fr); } }** - _Nagy képernyőn három oszlopban jelennek meg a cikkek._

**@media (max-width: 600px) { article { grid-template-columns: 1fr; } }** - _Kis képernyőn minden cikk egymás alá kerül._

## Tartalomdobozok oldal1 (article+.cikk)

**direction: rtl** - _a grid elemek jobbról balra kezdődnek, így például a 3. cikk előre kerülhet a vizuális sorrendben._

**.cikk{ direction: ltr; }** - _A .cikk tartalmát visszaállítjuk balról jobbra, így a belső tartalom normál sorrendben jelenik meg, függetlenül az article jobbról-balra beállításától._

## Reszponzív menü és tartalom

**center; gap: 1rem; } article { grid-template-columns: 1fr; } }** - _Kis képernyőn a menü egymás alá kerül, középre igazítva. A cikkek egy oszlopban jelennek meg, hogy jobban illeszkedjen a mobil kijelzőhöz._

**@media (min-width: 800px) { article { grid-template-columns: repeat(3, 1fr); } }** - _Nagy képernyőn a cikkek három oszlopban jelennek meg_