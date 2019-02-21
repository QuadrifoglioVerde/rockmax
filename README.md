Návod pro vytvoření vlastního skillu k přehrátí rádia RockMax na Amazon Echo :-)

1. Jdeme na https://developer.amazon.com/alexa/console/ask pokud nemáme účet, vytvoříme si jej.

2. Vytvoříme nový skill (Create Skill)

3. Vyplníme následovně:

	Skill name: rockmax
	Default Language: English (UK) nebo English (US), záleží jaký jazyk máme nastavený na Echu
	Vše ostatní necháme výchozí (Model - Custom, Method - Self Hosted)
	Pokračujeme dál (Create skill)

4. Vybereme výchozí možnost (Start from scratch) a jdeme dál...

5. V levém menu máme položku "Invocation",
	Zde nastavíme Skill invocation name: rockmax (tj, slovo na které alexa bude reagovat)
	Nyní položka JSON Editor, zde vložíme obsah souboru models/en-GB.json

	Klikneme na "Save Model"

6. Dále Interfaces, zde povolíme "Audio Player"
	Klikneme na "Save Interfaces" a "Build Model"

7. Položka "Endpoint" bude obsahovat AWS Lambda ARN:
	"arn:aws:lambda:eu-west-1:063544920746:function:rockmax-live"

Klikneme na "Save Endpoints"


A teď už by jsme měli vidět mezi skilly jeden vlastní, stačí povolit (pokud není)
a vyzkoušet "Alexa, play rockmax" nebo "Alexa, start rockmax" případně se alexy zeptáme "Alexa, ask rockmax what is playing"

A to je celá sranda :)
