---
no_native_review: true
---

# BanchoBot

*Niet te verwarren met [Bancho (server)](/wiki/Bancho)*

![BanchoBot's gebruikerskaart](img/BanchoBot.jpg "BanchoBot's gebruikerskaart")

**BanchoBot** (ook gekend als *Bancho*) is een online chatbot ontwikkeld voor osu!, die mensen in de in-game chat helpt door spelgerelateerde mededelingen te versturen (bv. totaal aantal keer gespeeld, aantal pogingen, enz.) en door te reageren op bepaalde opdrachten. BanchoBot werd geprogrammeerd door [Echo](https://osu.ppy.sh/users/431) en is de provider van de [Bancho IRC](/wiki/Internet_Relay_Chat) (Internet Relay Chat). 

BanchoBot heeft ook z’n eigen [osu! profiel](https://osu.ppy.sh/users/3) en [Twitteraccount](https://twitter.com/banchoboat)!

## Opdrachten

*Voor een lijst van opdrachten binnen de in-game client, zie: [Chatconsole](/wiki/Chat_Console#commands-list)*

BanchoBot kan reageren op opdrachten van spelers door te antwoorden op berichten in de chat. Alle BanchoBot-opdrachten beginnen met een uitroepteken (`!`), gevolgd door de naam van het commando die niet hoofdlettergevoelig is (zonder spaties ertussen). Deze commando's kunnen gebruikt worden in chatkanalen en in privéberichten met Bancho.

Als een normale gebruiker een commando in een publiek chatkanaal verstuurt, zullen andere gebruikers dit niet kunnen zien. Het antwoord op dit commando wordt verstuurd via een privébericht van Bancho. Gebruikers mogen ook het `/bb`-chatcommando gebruiken om automatisch een gesprek met BanchoBot te starten zodat ze hun opdrachten meteen kunnen versturen.

Hieronder zijn alle BanchoBot commando's opgelijst:

- [Help](#help)
- [Roll](#roll)
- [Stats](#stats)
- [Where](#where)
- [FAQ](#faq)
- [Report](#report)

### Help

```
!help
```

`!help` toont een lijst van alle beschikbare BanchoBot-opdrachten. Hieronder een voorbeeld van hoe deze opdracht gebruikt wordt:

```
13:00 pippi: !help
13:00 BanchoBot: Standard Commands (!COMMAND or /msg BanchoBot COMMAND):
13:00 BanchoBot: WHERE <user>
13:00 BanchoBot: STATS <user>
13:00 BanchoBot: FAQ <item>|list
13:00 BanchoBot: REPORT <reason> - call for an admin
13:00 BanchoBot: REQUEST [list] - shows a random recent mod request
13:00 BanchoBot: ROLL <number> - roll a dice and get random result from 1 to number(default 100)
```

### Roll

```
!roll <argument>/<getal>
```

`!roll` trekt een willekeurig getal van 1 tot het geselecteerde getal. Als er geen getal of argument wordt ingegeven, wordt 100 als maximumgetal gebruikt. Hieronder voorbeelden van hoe deze opdracht gebruikt wordt:

```
13:00 pippi: !roll 1000
13:00 BanchoBot: pippi rolls 109 point(s)
```

```
13:01 pippi: !roll kans op mislukking
13:01 BanchoBot: pippi rolls 75 point(s)
```

### Stats

```
!STATS <gebruikersnaam>
```

`!stats` toont de statistieken van de gebruiker die ingegeven werd. De uitvoer van dit commando hangt af van de [spelmodus](/wiki/Game_Modes) die de gebruiker voor het laatst speelde, alhoewel BanchoBot niet zegt van welke spelmodus deze statistieken afkomstig zijn. Als BanchoBot gevraagd wordt om de statistieken van een gebruiker die nog nooit osu! gespeeld geeft weer te geven, zal het antwoord `User not found` zijn, zelfs al bestaat die gebruiker wel. Hieronder een voorbeeld van hoe deze opdracht werkt:

```
13:01 pippi: !stats peppy
13:01 BanchoBot: Stats for peppy:
13:01 BanchoBot: Store: 427,514,691 (#94718)
13:01 BanchoBot: Plays: 7348 (lv66)
13:01 BanchoBot: Accuracy: 87.13%
```

### Where

```
!where <gebruiker>
```

`!where` toont de huidige locatie van de gebruiker die ingegeven werd. Standaard toont dit enkel het land van de gebruiker, maar als de gebruiker `Deel je woonplaats met anderen` heeft ingeschakeld, zal ook hun stad weergegeven worden. Hieronder een voorbeeld van hoe deze opdracht werkt:

```
pippi: !where Ephemeral
BanchoBot: Ephemeral is in Australia
```

### FAQ

```
!faq <invoer>
```

```
!faq list
```

`!faq` toont de toelichting die bij een ingevoerd onderwerp hoort. Het `list`-argument kan ook gebruikt worden om alle beschikbare onderwerpen te tonen. BanchoBot zal standaard antwoorden in het Engels, maar het is mogelijk om dit antwoord in een andere taal te ontvangen door de [tweelettercode](/wiki/Article_Styling_Criteria#locales) van die taal voor het onderwerp te voegen. Hieronder voorbeelden van hoe deze opdracht gebruikt wordt:

```
13:03 pippi: !faq peppy
13:03 BanchoBot: peppy is the lead developer and indeed, the creator of osu! and handles most of the project himself.
```

```
13:04 pippi: !faq ru:lines
13:04 BanchoBot: Умещайте свои мысли в меньшее количество строк, чтобы не получить сайленс.
```

### Report

*Voor informatie over wat het waard is om te rapporteren, zie [Ongepast gedrag rapporteren](/wiki/Reporting_Bad_Behaviour)*

```
!report <gebruiker> <reden>
```

`!report` brengt het [Wereldwijde Moderatieteam](/wiki/Global_Moderation_Team) op de hoogte van het ongepaste gedrag van een gebruiker. Als een gebruiker spaties in hun naam heeft, vervang ze dan door underscores (bv. `heel coole gebruikersnaam` wordt `heel_coole_gebruikernaam`). Verzend een e-mail naar [support@ppy.sh](mailto:support@ppy.sh) om een moderator te rapporteren. Hieronder een voorbeeld van het rapporteren van een normale gebruiker via BanchoBot:

```
13:10 pippi: !report flyte spamming in #japanese
13:10 BanchoBot: Chat moderators have been alerted. Thanks for your help.
```

## Trivia 

- De gebruikerspagina van BanchoBot heeft "Here since the beginning" als toetredingsdatum
  - De officiële toedredingsdatum van BanchoBot is 22:09:14 UTC-5, 27 augustus 2007
