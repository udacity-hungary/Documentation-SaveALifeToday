## Lottó app

### Ötlet
A lottószelvényt lefényképezzük, felismerjük a rajta lévő számokat, érvényességi időt, stb, ezt elmentjük egy adatbázisba (lokál), majd a sorsolás után összenézzük a kihúzott számokat az eltárolt értékekkel, és küldünk egy értesítést, hogy nyert-e a szelvény.

### Megvalósítás
* Activity 1: az érvényes szelvényeink listája, esetleg figyelmeztetéssel hogy hamarosan le fog járni.
* Activity 2: új szelvény hozzáadása; fénykép, karakterfelismerés (egyáltalán ismerjük fel, hogy szelvényt fotóztunk), a felismert értékek (számok, érvényességi idő) mutatása szerkesztési lehetőséggel (ha hibás a felismerés, akkor meg lehessen adni kézzel az adatokat).
* Activity 3: beállítások (gondolom lehet dolgokat állítgatni)
* Adatbázis: tárolja a mentett értékeket.
* Background/scheduled task: húzások után pollozza a kihúzott számokat és elkészíti a notificationt.

### Kockázatok
* Nincs tapasztalatom a Vision Library-vel, bár állítólag könnyű, tehát valaki(k) esetleg meg is tanulhatná(k).
* Azt hiszem a Play Store-ba nem lehet feltölteni szerencsejátékokat, bár ez az App nem konkrétan szerencsejáték (nem mi szervezzük a játékot), csak a nyomonkövetésére szolgál.
* A kihúzott számok listája jól olvasható formátumban letölthető a szerencsejatek.hu-ról. Nem lenne jó, ha kitiltanák onnan az alkalmazást, bár elvileg elég heti egyszer letölteni, és akár egy külön szerverre is menthetnénk a számokat (tényleg heti egyszer) és a mi szerverünket pollozhatná az app. Mindenesetre ez is egy kockázat, hogy hogyan szerezzük meg a számokat.
* Az appot a külföldi kollégák nem nagyon fogják tudni tesztelni magyar lottó híján. Persze lehet bele tenni Eurojackpot supportot is (feltéve, hogy annak minden országban ugyanolyan a nyomtatott formátuma), viszont azt nem tudom, hogy Eurojackpont számok vannak-e a szerencsejatek.hu-n, tehát lehet keresni kell más forrást.



# Eltűnt kisállat app

## Ötlet

Az alkalmazásban gazdik jelezhetnék, ha eltűnt kisállatuk, illetve talált, kóborló állatokról lehetne fényképet, leírást akármit készíteni és feltölteni. A feltöltött adatokat hely alapon is lehetne szűrni.

## Megvalósítás

* Activity_1: A keresett, megtalált állatok böngészése mindenféle szempont szerint
* Activity_2: Bejelentő lap, megtalálás, eltűnés bejelentése kép- és adatfeltöltéssel
* Activity_Stats: Lehetne egy olyan felület, ami mutatja az app által megtalált állatok számát, meg hasonlókat, ez lehet egy kis kedvcsináló. Sőt, ha van rá igény, itt lehetne akár userStats is, ami esetleg ösztönöz az aktivitásra.
* Preferences_Activity: minden, ami értesítés, plusz személyes adatok, plusz engedélyek   
* Service: Ha van net (mobil, wifi beállítás alapján) frissíti hely alapon a keresett, megtalált állatok listáját, ha úgy van beállítva, akár értesítést is dob a felhasználónak.

## Kockázatok

Az app nem csak androidos fejlesztést foglal magában, hanem egy webes felületre is szükség van legalább API és adatbázis szintjén, úgy gondolom, ez a kockázat lehetőség is egyben, hiszen a tartós üzemeltetéshez meg lehet keresni állatvédő szervezeteket, akik remélhetőleg örömmel fogadják, használják és népszerűsítik az appot.

## Megjegyzések

Ha valami elkerülte a figyelmem, ide írd be nyugodtan.

## Footer

A talált és eltűnt állatok GPS koord-al történő helymeghatározása, illetve a bejelentések egyedi megosztási lehetőségeinek elősegítése is fontos lehet a közösségi oldalakon vagy olyan személyekkel, akiket érdekelhet az információ. 
/az állatvédő szervezetek és menhelyek bevonásával az állatok adoptálásának elősegítésére is lehetőség lenne/ 



# Fuss közösségi célért app

## Ötlet

Az alkalmazásban rögzíteni tudod, ha futsz. Ez a része egy klasszikus futós app, ugyanakkor a futásodat felajánlhatod közösségi cél érdekében, ha van, aki a megtett kilométer, eltelt idő, elégetett kalória vagy épp a rendszeresség alapján ezt támogatja.

## Megvalósítás

* Activity_1: Személyes statok, mennyit futottál, mennyi idő alatt, hány kalóriát égettél el, mennyire mozogsz rendszeresen, kiket támogattál eddig és milyen mértékben.
* Activity_2: Térképes rész, ami a kedvenc futós helyeidet, esetleges egyéb jótékony vagy sima futásokat tartalmazza
* Activity_Stats: megmutatja, hogy állnak az egyes gyűjtések, lehetnek ranglisták, stb.
* Preferences_Activity: Saját fiók beállítása és minden más.

## Kockázat

Ilyen app már létezik, méghozzá valamelyik Udacity kurzus anyagában láttam - de nem tudok rájönni, hol és ki sem tudtam guglizni, hogy hívják. Lehet, azért nem, mert időközben megbukott a projekt. 😞 

Másik nehézség/kockázat, hogy ehhez támogató kell, bár az egészséges élet olyasmi, amihez tudnánk támogatót találni. Egyesületet pedig tudok, aki felvállalná az app menedzselését.

## Megjegyzések

Feel free to add some more idas or comments.

A létező app, ha jól emlékszem a Charity Miles volt.



**Ötlet:**
Egy alkalmazáson belül rögzíthető lenne, hogy betegség esetén a felhasználó milyen gyógyszereket szed, milyen kezeléseket kap, valamint a kapott dokumentumokat tárolhatja (praktikus OCR-rel). Ezekből bármilyen időszakra vonatkozóan komplett gyógyszer és kezeléstörténet statisztikákat lehetne készíteni. A gyógyszerekhez időzítő rendelhető, az app jelez, hogy mikor, mit és mennyit kell bevenni.

**Megvalósítás:**
Egyéni preferencia, én szeretem a tab-os megoldást, de lehet,h ogy más lesz parktikusabb.
- bejelentkezési felület: itt megadható adatok (kor, nem, egyéb, amit hasznosnak ítélünk)
- Gyógyszerek: itt hozzáadhatóak és időzíthetőek a gyógyszerek (notification)
- Kezelések: kezelés típusa, helyszíne (Google Maps), időpontja (notification) rögzíthető
- Dokumentumok: kezelési naplók, zárójelentések, beutalók, egyéb kacsolódó dokumentumok rögzíthetők, tag-ekkel elláthatók
- Stat: itt adott időintervallumra szűrve lekérhető az előzőekből bármelyik adat

**Kockázat:**
Az adattárolásról nem írtam a megvalósításnál. Mivel nagyon érzékeny adatokról van szó, át kell gondolni a pro és kontra érveket a helyi illetve felhős adattárolás esetében, és ez alapján dönteni.
Komoly százalékban olyan korosztályt érint a téma, akik nem feltétlenül használnak okostelefont.
TAJ nyilvántartásban ügyfélkapuval lekérdezhető a betegéletút. Viszont egy konkrét, mindig zsebben hordott app kényelmesebb, testreszabhatóbb, könnyebben elérhető. Ettől függetlenül hosszú távon akár működhetne együtt is a két dolog.

 

Here and now! - munkacím

Az alkalmazás indítása után  megjelenik Activity 1, három teljes kijelzős fragmenttel (view pager? bottom navigation?). Az első fragment rácsszerkezetben megmutatja az adott földrajzi lokációban legutóbb készült 9/16/24/bármennyi instagram fotót. Fotóra kattintva (Activity 2) megjelenik a kép, kommentekkel meg minden (esetleg indítja az instagram appot).
 
Activity 1 második fragmentjén az adott földrajzi lokációban gyakran használt hashtegeket mutatja list formában, azokra kattintva (Activity 3) az adott földrajzi lokációban az adott hashteggel készült fotókat mutatja az Activity-1/fragment1-hez hasonló layout-ban. Fotóra kattintva  megjelenik a kép, kommentekkel meg minden (esetleg indítja az instagram appot).

Activity 1 harmadik fragmentjén az adott földrajzi lokáció legnépszerűbb fotóit jeleníti meg az app, Fragment1-hez hasonló szerkezetben. Fotóra kattintva  megjelenik a kép, kommentekkel meg minden (esetleg indítja az instagram appot).

Kockázatok: Instagram API. Van, de nem tudom mik a terhelhetősége határai, illetve mennyire komplex kereséseket enged meg (lokáció+népszerűség, lokáció+hashtag, lokáció+frissesség). 

Az app teljesen haszontalan és öncélú :) Engem pont érdekel, hogy egy adott területen milyen fényképek készültek, mi ragadta meg ott az emberek figyelmét, mit hoztak ki belőle, satöbbi. Mást meg pont nem :) Viszont elég komplexnek tűnik ahhoz, hogy jó gyakorló feladat legyen és elég egyszerűnek ahhoz, hogy hamar megvalósítható legyen. 



Ma nap közben már nem lesz időm kifejteni ezt jobban. Megjelöltem, hogy szerintem melyik lenne a legjobb. Ha a játékot választjátok, akkor kifejtem este részletesebben alapesetben azt, vagy ha közben Slack-en meggyőztök egy másikról, akkor egy másikat.

Ezekből majd egyet kifejtek, egyelőre ötlet szinten:

* Ki nevet a végén? (Ludo) - ebből sok van, de pl. 6-személyes kevés, és meg lehet csinálni genya AI-val jó nehézre is
* Memóriajáték (lefordított lapokat forgatunk kettesével és párokat kell találni)
* **Memóriajáték variáció: a lapok elmászkálnak közben**
* * Beállítható tábalméret
* * állítható / véletlenszerű képcsomagok
* * több háttérkép, több kártyaháttér, zene, effektek, animációk, bármi jöhet, semmi sem kötelező :-)
* * rekordok tárolása (hány fordításból találtad ki)
* * pontozás, akár achievementek (pl. 10 játékot megcsináltál 20 lépés alatt egymás után), stb, stb
* [Sliding puzzle](https://en.wikipedia.org/wiki/Sliding_puzzle)
* Sliding puzzle variáció: [Klotski](https://en.wikipedia.org/wiki/Klotski)



## Mozogj egyszerre app

### Ötlet
Mostanában elég sok cikk van arról mennyire káros a tablet/mobil, mert csak gubbaszt vele az ember, készíthetnénk egy olyan appot ami időről időre mozgásra ösztönzi a felhasználókat, esetleg közösségi eseményként egy-egy event 12:00-tól jóga légzés, csatlakozz :slightly_smiling_face: vagy menjünk futni 30 perc, csatlakozz, 5 perc plank. Vicces lenne egy irodában pl a random feladatok elvégzése, és lehetne vele pontokat gyűjteni, ma mennyire voltál aktív ki a legjobb...




# Ötlet : 112 segélyhívó
Az appba regisztrált személyeket a felmerülő vészhelyzet (elsősegély kérés, tűz, rablás, erőszak, műszaki mentés) jellege alapján az app segítséghez juttatja. A felmerülő segítségkérő igény kezeléséhez a www.112.hu egységes segélyhívó szervezet operátorával működhetne együtt az alkalmazás.
# Megvalósítás
## Navigation Drawer + viewpager
### Navigation Drawer menü főbb elemei:
* főoldal
* felhasználói profil beállítása: személyi adatok, egészségügyi adatok, 
* beállítások: a telefon egyedi hang, hosszan nyomás, vagy rázás hatás érzékelésének beállítási lehetősége, instant üzenetek rögzítési lehetősége különböző helyzetekre
* 112: diszpécserszolgálat vagy szolgáltató tájékoztató adatai ahová befut a jelzés szervezetek, vagy magánszemély, akinek a részére szintén érdemes üzenetet küldeni
* szokásos menü elemek: elérhetőség, kilépés esetleg smart watch funkciók 

### View pager lapok:
* főoldal: veszély jelzési gombok, melyek érintésekor a megfelelő üzenet továbbításra kerül, a 112 – operátorának, vagy a megadott magánszemélynek GPS koordinátákkal együtt
* térkép: saját hely beállításhoz, útvonaltervezéshez 
* közösségi funkciók használata: üzenetváltás  a 112 operátoraival, megosztás
+ lebegő leállító gomb, arra az esetre ha időközben mégsem szeretnénk küldeni a jelzést

# Kockázat
Az app első fázisát érdemes lenne csak a 112 -re alapozni, kérdés, hogy kiadták – e már valakinek az app megvalósítását. Magyar piac befogadja e. 
