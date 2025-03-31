# Utläggshantering för ledare

## Översikt

Utläggsfunktionen låter ledare och scouter registrera, hantera och få ersättning för utlägg kopplade till scoutaktiviteter. Funktionen ger ledare möjlighet att hantera hela processen från registrering till utbetalning och bokföring.

## Innehåll

1. [Komma igång](#komma-igång)
2. [Utläggslistan](#utläggslistan)
3. [Skapa ett nytt utlägg](#skapa-ett-nytt-utlägg)
4. [Automatisk tolkning av kvitton](#automatisk-tolkning-av-kvitton)
5. [Granska och hantera utlägg](#granska-och-hantera-utlägg)
6. [Statusar för utlägg](#statusar-för-utlägg)
7. [Exportera till Google Sheets](#exportera-till-google-sheets)
8. [Vanliga frågor](#vanliga-frågor)

## Komma igång

För att komma åt utläggsfunktionen, navigera till din avdelnings sida och klicka på "Utlägg" i sidomenyn. Detta visar avdelningens utläggslista.

## Utläggslistan

Utläggslistan visar alla utlägg kopplade till din avdelning, sorterade efter datum med de nyaste utläggen först. Härifrån kan du:

- **Filtrera utlägg** efter status (Alla, Väntande, Godkända, Avslagna)
- **Se totalsumman** för alla godkända utlägg (visas när filtret "Godkända" är aktivt)
- **Skapa nya utlägg** genom att klicka på "Registrera utlägg"
- **Visa detaljer** för ett specifikt utlägg genom att klicka på datumet

För varje utlägg visas följande information:
- Datum
- Beskrivning
- Belopp
- Scout (vem som begärt ersättning)
- Status (väntande, godkänd eller avslagen)

## Skapa ett nytt utlägg

Som ledare kan du registrera utlägg både för dig själv och för scouter i din avdelning.

1. Klicka på "Registrera utlägg" från utläggslistan
2. Ladda upp ett kvitto genom att klicka på "Lägg till kvitto"
3. Välj vilken scout utlägget gäller för från rullgardinsmenyn
4. Fyll i följande obligatoriska information:
   - **Datum** (när utgiften inträffade)
   - **Belopp** (måste vara större än 0)
   - **Beskrivning** (vad utgiften avser)
   - **Valuta** (standardvärde är SEK)
5. Swishnummer hämtas automatiskt från scoutens registrerade telefonnummer
6. Klicka på "Spara" för att skapa utlägget

## Automatisk tolkning av kvitton

Systemet använder AI för att automatiskt tolka uppladdade kvitton:

1. När du laddar upp ett kvitto (bild eller PDF) analyseras innehållet
2. Systemet extraherar automatiskt:
   - Totalt belopp
   - Datum
   - En lämplig beskrivning
   - Valuta
3. De extraherade värdena fyller automatiskt i formuläret
4. Du kan redigera all information innan du sparar utlägget

Funktionen stödjer både bilder och PDF-filer. PDF-filer konverteras automatiskt till bilder för analys.

## Granska och hantera utlägg

För att hantera ett utlägg:

1. Klicka på utläggets datum i utläggslistan
2. På detaljsidan kan du:
   - Se all information om utlägget
   - Visa det uppladdade kvittot (klicka för att förstora)
   - Redigera utlägget genom att klicka på "Redigera utlägg"
   - Ändra status genom att klicka på "Ändra status"
   - Ta bort utlägget vid behov

## Statusar för utlägg

Utlägg kan ha tre olika statusar:

- **Väntande (pending)**: Utlägget har registrerats men inte hanterats än
- **Godkänd/Betald (paid)**: Utlägget har godkänts och ersättning har betalats ut
- **Avslagen (rejected)**: Utlägget har avslagits och ersättning kommer inte att betalas ut

För att ändra status:

1. Öppna utlägget och klicka på "Ändra status"
2. Välj önskad status i dialogrutan
3. Klicka på "Spara"

När ett utlägg markeras som betalt, exporteras det automatiskt till avdelningens ekonomiblad i Google Sheets.

## Exportera till Google Sheets

När ett utlägg markeras som betalt exporteras följande information automatiskt till avdelningens flik i kårens ekonomiblad:

- Datum
- Beskrivning
- Scoutens namn (med länk till scoutprofilen)
- Belopp
- Uppdaterat saldo
- Länk till utläggsdetaljer och kvitto

Utlägget markeras sedan som exporterat i systemet för att undvika dubbelexport.

## Vanliga frågor

### Hur ändrar jag ett utlägg som redan sparats?
Öppna utlägget genom att klicka på datumet i utläggslistan och välj sedan "Redigera utlägg".

### Kan jag registrera ett utlägg utan kvitto?
Nej, ett kvitto är obligatoriskt för alla utlägg.

### Vad gör jag om den automatiska tolkningen av kvittot är felaktig?
Den automatiska tolkningen är ett hjälpmedel. Du ska alltid kontrollera informationen och korrigera eventuella fel innan du sparar utlägget.

### Hur vet jag om ett utlägg har exporterats till ekonomibladet?
På utläggets detaljsida finns information om huruvida utlägget har exporterats eller inte.

### Kan en scout själv registrera ett utlägg?
Ja, scouter kan registrera utlägg via sin egen inloggning. Dessa utlägg hamnar sedan i avdelningens utläggslista för godkännande av ledare. 
