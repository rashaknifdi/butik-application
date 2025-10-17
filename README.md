# 🛍️ ButikApp

## 📌 Om projektet
Detta är ett Java-projekt jag har byggt som en del av min inlämningsuppgift.  
Applikationen simulerar ett enkelt försäljningssystem för en butik där man kan lägga till produkter, skapa ordrar och analysera försäljningsdata.  
Programmet körs i konsolen och är uppbyggt enligt SOLID-principerna med fokus på robust kod, loggning och tydlig struktur.

---

## 🛠️ Teknik jag har använt
- Java 17
- Maven för bygg och körning
- SLF4J för loggning
- Logback för att spara loggar i fil
- Stream API för filtrering, sortering och analys
- Egna undantagsklasser för affärslogik
- Datastrukturer: `List`, `Map`

---

## 🧱 Datastrukturer
Jag har valt följande datastrukturer:

- `List<Product>` – för att lagra alla produkter i systemet
- `List<Order>` – för att lagra alla ordrar
- `Map<String, List<Order>>` – för att gruppera ordrar per kundnamn där nyckeln är kundnamnet och värdet är deras orderhistorik

Jag valde dessa eftersom de ger enkel åtkomst, sortering och filtrering med Stream API, och passar bra för den typ av data som hanteras.

---

## 🔄 Stream-funktioner
Jag har implementerat tre funktioner med Stream API:

- Filtrera produkter per kategori och sortera efter pris
- Beräkna totalvärdet av en kunds orderhistorik
- Hitta de tre mest köpta produkterna totalt

Alla funktioner är kommenterade och motiverade i koden.

---

## 🚨 Undantagshantering
Jag har skapat flera egna undantag för att hantera affärslogikfel:

- `EmptyOrderException` – om användaren försöker skapa en tom order
- `InvalidPriceException` – om priset är negativt
- `NoOrdersForCustomerException` – om en kund saknar ordrar
- `NoProductsInCategoryException` – om en kategori är tom
- `NoProductsFoundException` – om det inte finns några produkter i systemet
- `NoOrdersFoundException` – om det inte finns några ordrar att analysera

## 👤 Utvecklare
- Namn: Rasha Knifdi

- Roll: Fullstack Java Student