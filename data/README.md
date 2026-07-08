# UniMatchr — datafil

Sidan läser `universities.csv` i den här mappen. Redigera den så uppdateras sidan
(du kan ändra direkt här på GitHub via pennan ✏️, eller öppna filen i Excel/Google
Sheets, spara som CSV och committa — eller bara säg till Claude så fyller han på).

En rad = ett universitet. Kolumnernas **rubriknamn får inte ändras** (sidan slår upp
dem på namn), men du kan lägga till rader fritt.

## Kolumner

| Kolumn | Vad | Exempel |
|--------|-----|---------|
| `id` | Valfritt kort id (landskod + nummer) | `NL001` |
| `name` | Universitetets namn | `Utrecht University` |
| `country` | Land | `Netherlands` |
| `city` | Stad (styr även bilden, se nedan) | `Utrecht` |
| `continent` | Världsdel — används i filtret | `Europe`, `Asia`, `Africa`, `North America`, `Oceania` |
| `language` | Undervisningsspråk | `English` |
| `freemover` | **Kärnfältet.** Tar de emot freemovers? | `Yes`, `No` eller `Limited` |
| `cost_band` | Grov kostnadsnivå för en freemover-termin | `Free`, `Low`, `Medium`, `High` (eller tomt) |
| `website` | Länk till skolans sida för detaljer | `https://...` |
| `subjects` | Ämnen, kommaseparerade — styr sök & taggar | `Business, Law, Engineering` |
| `note` | Kort notis (visas på kortet) | `Fee-paying study abroad, two intakes/year.` |

### Kostnadsnivåer (`cost_band`)
Ungefärlig avgift för freemovers per termin:
- **Free** – ingen terminsavgift (ofta nordiska statliga universitet)
- **Low** – upp till ~2 000 €
- **Medium** – ~2 000–5 000 €
- **High** – över ~5 000 €

Lämna tomt om du inte vet — sidan visar då `—`.

### Bilder
Kortets bild hämtas automatiskt från `images/cities/<stad>.jpg` (gemener, bindestreck
istället för mellanslag/specialtecken, t.ex. `San Diego` → `san-diego.jpg`). Saknas
bilden visas kortet ändå, bara utan bild. Säg till Claude så hämtar han en ny stadsbild.
