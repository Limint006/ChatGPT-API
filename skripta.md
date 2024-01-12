# ChatGPT-API

## Co je to ChatGPT API?
ChatGPT API je rozhraní pro programování aplikací (API), které umožňuje vývojářům integrovat model ChatGPT do svých vlastních aplikací, produktů nebo služeb. OpenAI poskytuje toto API jako službu, která umožňuje přístup k jazykovým modelům (například v naší ukázce GPT-3.5) pro generování textu a odpovědí na různé dotazy.


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
Zde se snažíme vytvořit odpověď (response). Začneme tím, že vybereme model, který má být použit, a poté do něj vložíme informace. Tyto informace se dělí do tří druhů:

"system" Pomáhá nastavit chování asistenta. Například můžete upravit osobnost asistenta nebo poskytnout konkrétní pokyny k jeho chování během konverzace.

"user" Obsahuje požadavky nebo komentáře, na které má asistent reagovat.

"assistant" Ukládá předchozí odpovědi asistenta, ale mohou být také napsány vámi k poskytnutí příkladů požadovaného chování.

### Základní program
![aaaaacode](https://github.com/Limint006/ChatGPT-API/assets/114061078/56eefaf4-2d6f-4209-b78b-608094ad6c2c)
Teď se základními znalostmi můžeme začít psát kód.

Začneme importováním openAI knihovny: `from openai import OpenAI`

Abychom mohli využívat API, musíme mít i klíč: `OpenAI.api_key = "VÁŠ KLÍČ"`

V tomto příkladu využíváme string message, do kterého píšeme přes terminal jako vstup, pro již zmíněný proces tvorby odpovědi.

A nakonec vypíšeme odpověď. Tu vytáhneme z naší proměnné tímto způsobem: `response['choices'][0]['message']['content']` Celý výstup ale vypadá takto:
![aaaaaaacode](https://github.com/Limint006/ChatGPT-API/assets/114061078/798320db-9aa0-4ac0-8607-6f0f8b283dfc)

### Optimalizovaný program

![aaacode](https://github.com/Limint006/ChatGPT-API/assets/114061078/bc8299bf-17a9-4de9-b975-ed0ab743e420)
Mezi tímto a předchozím kódem existují dvě odlišnosti.

První rozdíl spočívá v tom, že v kódu není přímo viditelný API klíč. Ten je uložen v souboru ".env". Do tohoto souboru zapište `OPENAI_API_KEY=VÁŠKLÍČ`, a v hlavním souboru je poté voláno pomocí `dotenv.load_dotenv()`.

Druhý rozdíl spočívá v ukládání celé konverzace do pole "messages", což umožňuje chatbotovi pamatovat si předchozí zprávy. Toto bylo dosaženo pomocí `messages.append`.

## Závěr
Díky těmto krokům jsme úspěšně připravili prostředí pro práci s ChatGPT API. Po nainstalování potřebných knihoven a získání API klíče můžeme začít psát kód a interagovat s modely. Ujistěte se, že máte připravené systémové a uživatelské zprávy pro lepší kontrolu chování asistenta. Celkově jsme nyní připraveni vytvářet a zlepšovat konverzace s ChatGPT API. Happy coding!
