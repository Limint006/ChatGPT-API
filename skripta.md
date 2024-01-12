# ChatGPT-API

## Co je to ChatGPT API?
ChatGPT API je rozhraní pro programování aplikací (API), které umožňuje vývojářům integrovat model ChatGPT do svých vlastních aplikací, produktů nebo služeb. OpenAI poskytuje toto API jako službu, která umožňuje přístup k jazykovému modelu GPT-3.5 pro generování textu a odpovědí na různé dotazy.


## Jak to funguje?
ChatGPT API pracuje na základě žádostí a odpovědí. Vývojář může posílat textové dotazy do API a obdrží generované odpovědi od modelu GPT-3.5. V každé žádosti může vývojář specifikovat vstupní kontext, který model používá k porozumění a generování odpovědi.


## Cena?
Po vytvoření účtu na OpenAI obdržíte úvodní kredit ve výši 18 $. Tento kredit vám poskytuje dostatečné finanční prostředky na delší dobu, neboť náklady na položení otázky jsou zlomky centů.

Na obrázcích níže vidíme, jak nízké jsou náklady na konkrétní operace v rámci ChatGPT API.
![image](https://github.com/Limint006/ChatGPT-API/assets/114061078/5a14456b-8a82-4314-b952-ab4c1a600920)
![image](https://github.com/Limint006/ChatGPT-API/assets/114061078/0f87a5c9-77d9-4cd0-a723-1e5368683f42)


## Jak nastavit ChatGPT API?
### Nainstalování knihoven do počítače
V tomto návodu budeme využívat Python ve vývojovém prostředí Visual Studio Code. Po zapnutí příkazového řádku napište následující:

`pip install openai python-dotenv`

Tímto způsobem jsme úspěšně nainstalovali všechny potřebné knihovny pro základní práci s ChatGPT API.

### Získání klíče
Nejdůležitějším krokem je vytvoření účtu na OpenAI. Navštivte stránky https://platform.openai.com a vytvořte si účet nebo se přihlaste, pokud již účet máte (Využijte stejný účet, který využíváte, když si píšete s ChatGPT). Po vytvoření účtu se v levém menu objeví přístup k vašemu účtu. Přejděte do záložky "API Keys" a zde vytvořte klíč, který budeme používat pro další kroky.

![image](https://github.com/Limint006/ChatGPT-API/assets/114061078/9e6fac5c-6f3d-42af-8289-98ef0ad47c6a)


## Jak s tím pracovat?
### Základní pojmy
![aacode](https://github.com/Limint006/ChatGPT-API/assets/114061078/a99d6fab-c7f6-4513-83f3-19660df550b0)


### Základní program
Když už máme knihovny i klíč, tak můžeme začít psát kód. 

![aacode](https://github.com/Limint006/ChatGPT-API/assets/114061078/a2c5721b-5eee-4ccd-90c3-e5c88473d92b)

Začneme importováním openAI knihovny: `from openai import OpenAI`

![acode](https://github.com/Limint006/ChatGPT-API/assets/114061078/5185a18d-7347-45b8-90b9-c5f40a7fac50)


