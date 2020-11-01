# Internet Relay Chat

[Internet Relay Chat](https://en.wikipedia.org/wiki/Internet_Relay_Chat), beter bekend als IRC, is een uitgebreid en gestandardiseerd protocol om te chatten met verschillende clients waarmee verbonden kan worden.

## osu!Bancho

osu!Bancho is een gateway voor IRC-toegang (de in-game chat). Je kan ook verbinden via jouw eigen client, waardoor je kan chatten met anderen zonder de osu! client te gebruiken. Let erop dat het IRC-protocol ietwat aangepast werd, dus verwacht niet dat alle functies in jouw client correct zullen werken.

**Opmerking: [HexChat](https://hexchat.github.io/) staat erom bekend om problemen te hebben met osu!'s IRC** ([bug report van HexChats GitHub](https://github.com/hexchat/hexchat/issues/818)), overweeg een andere client te gebruiken als dit je stoort.

## Hoe verbinden

Wanneer je een client hebt gevonden, moet je de serverinstellingen nog invoeren.

- **Server:** `irc.ppy.sh`
- **Poort:** `6667` (standaard)
- **Gebruikersnaam:** Jouw osu! gebruikersnaam (vervang spaties door underscores)
- **Wachtwoord:** Ontvang jouw wachtwoord via [IRC-Authenticatie](https://osu.ppy.sh/p/irc).

*Jouw IRC-wachtwoord verschilt van jouw account wachtwoord. **Deel het niet met anderen**.*

## Standaard IRC-opdrachten

| Opdracht | Beschrijving |
| :-- | :-- |
| `/join <#kanaal>` | Treedt toe tot een kanaal |
| `/part <#kanaal>` | Verlaat een kanaal |
| `/me <actie>` | Verzendt een actiebericht |
| `/ignore <gebruikersnaam>` | Negeert een gebruiker (verbergt hun berichten) |

## Join/part-bericht uitschakelen

Soms is het goed om te weten wie toetreedt tot een kanaal of dit verlaat, maar in erg drukke kanalen zoals `#osu` zal je de hele tijd join/part-berichten ontvangen waardoor je het gesprek in de chat niet meer kan volgen. Daarom is het vaak beter om deze berichten te verbergen.

```
[17:46] * lauripihl (cho@ppy.sh) has left #lobby
[17:46] * Kastun (cho@ppy.sh) has joined #lobby
[17:46] * AuReL (cho@ppy.sh) has joined #lobby
[17:46] * osukd (cho@ppy.sh) has joined #lobby
[17:46] * BreadTooGood (cho@ppy.sh) has joined #lobby
[17:46] * keanyew18 (cho@ppy.sh) has joined #lobby
[17:46] * JaKox (cho@ppy.sh) has joined #lobby
[17:46] * Kerantor (cho@ppy.sh) has joined #lobby
```

### Join/part-bericht uitschakelen in veelvoorkomde clients

| IRC client | Beschrijving |
| :-- | :-- |
| [HexChat](https://hexchat.github.io/) | Ga naar Settings - Preferences, onder Chatting - General, vink "Hide join and part messages" aan |
| [ircII](http://www.eterna.com.au/ircii/) | Type `/ignore * crap` |
| [Irssi](https://irssi.org) | Typ `/ignore -channels #somechannel * JOINS PARTS QUITS` |
| [Weechat](https://weechat.org/) | Typ `/filter add irc_smart_weechat irc.gebruikersnaam.#channel irc_smart_filter *`. **Let op:** Vervang **gebruikersnaam** door jouw osu! gebruikersnaam. |
| [KVIrc](https://www.kvirc.net/) | Bekijk [dit artikel](http://www.kvirc.ru/forum/?topic=609.0) op het officiele KVIrc forum. |
| [mIRC](https://www.mirc.com/) | Ga naar mIRC Options (Tools - Options / Alt + O), onder IRC tree, klik op de "Events..."-knop en verander Joins and Parts naar "Hide" |
| [Quassel IRC](https://quassel-irc.org/) | Rechtsklik op het chatting-venster, kies daarna Hide Events » Join/Part/Quit. |
| [XChat](http://xchat.org/) | Typ `/set irc_conf_mode 1` (of [2](http://xchat.org/faq/#q211) om de berichten uit te schakelen doorheen alle kanalen). |

Bekijk de documentatie van jouw client als hij hierboven niet werd vermeld. De meeste clients hebben ergens een manier om deze berichten uit te schakelen.

## Veelgestelde vragen (FAQ)

### Ik krijg een foutmelding: "Bad Authentication Token"

1. Zorg ervoor dat je het wachtwoord van de [IRC Authenticatie](https://osu.ppy.sh/p/irc)-pagina gebruikt.
2. Vervang spaties door underscores als jouw gebruikersnaam spaties bevat. (bv. **Deze Gebruikersnaam** naar **Deze_Gebruikersnaam**)

### Kan ik een andere gebruikersnaam gebruiken?

Nee. Je kan enkel jouw osu! gebruikersnaam gebruiken.

### Waarom heb ik een voice status? Ik zie dat sommige mensen ook deze status hebben

Gebruikers met een *voice status* zijn ook verbonden via een IRC client, behalve chat moderators die altijd een *operator (+o)* status hebben, ongeacht welke client ze gebruiken.

Gebruikers die geen status hebben zijn verbonden via de in-game client.
