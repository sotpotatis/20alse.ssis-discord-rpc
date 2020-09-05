# SSIS Discord RPC

Ett enkelt skript som uppdaterar din status på Discord till den nuvarande lektionen på ditt schema. Konfigureras enkelt av vem som helst, även om du inte kan programmering.


### Vad är detta?

SSIS Discord RPC är ett kort skript jag skrev som använder sig av Discord Rich Presence. Under din skoldag kommer det, om skriptet körs och du har Discord som körs på din dator, visas "Spelar SSIS" som status för din profil. Om man klickar på denna status får man upp aktuell lektion, eller om du
har rast. Skriptet kan även detektera om du äter lunch.

### Tekniska förutsättningar

- Skrivet i Python med modulen pypresence. 

- Konfigurerbart på ett enkelt sätt.

- Hämtar endast meny och schema en gång per dag för att avlasta SSIS servrar.

### Installation

Följ dessa steg så är du igång på nolltid.

1. Om du inte redan har Python 3, ladda ner det. Kika [här](https://realpython.com/installing-python/)  för vidare hjälp med installationen.

2. Ladda ner detta projekt till din dator. Det kommer förmodligen ner som en .zip-fil - extrahera (packa upp) den.

3. Vi kör det jobbiga först - kommandotolken. Öppna en ny kommandotolk *i den mappen du nyss laddat ner* (detta är viktigt),
och skriv kommandot: `pip install -r requirements.txt`. Detta kommer installera allt annat som behövs för projektet.

Nu kommer det sista steget i konfigurationen - att konfigurera så att rätt schema används. Det är typ den enda konfigurationen som du **bör** göra,
sen kan du även fippla runt med lite andra parametrar om du känner dig modig. 

4. Öppna filen "config.ini" i undermappen "conf".

5. Ändra värdet under "schedule_name" till namnet på din klass, till exempel "``te20a`" eller `te18c`. Ja, du fattar.

6. Kör koden! Voilá. Tacka mig senare.


### Mini-FAQ 

#### Applikationsrelaterat:

###### Appen funkar inte!

DMa mig på Discord så löser vi det. Beskriv gärna mer än "Funkar inte". Vad händer exakt?

#### Kodrelaterat:

##### Lägg av Albin!!! Python suger bla bla bla bla

Jag har flera hemsidor med över 1000 klick om dagen som helt har Python som backend. Jag har inget emot Python alls då jag inte har behövt göra superhårda 3D-spel eller analyserat försäljningsdata över alla grönsaker på hela jorden. Om man nu skulle vilja klaga ändå och säga, "Python är bara för skript", så är detta faktiskt ett... skript. Koden är enkel att förstå och Python passade perfekt för denna typen av uppgift. Det går snabbt att skriva och snabbt at ändra.

##### Grr, vet du inte om Game Engine???

Jag känner till att Discord börjat med en ny "Game Engine" för custom status, men det verkar inte finnas stabilt stöd för det i något Python-bibliotek än. Då det bara är ett par rader kod som uppdaterar statusen så kommer jag ändra detta så fort det finns tillförlitligt stöd. Har jag tid kanske jag skriver en egen wrapper, men jag har hittat en i Python som är i beta.