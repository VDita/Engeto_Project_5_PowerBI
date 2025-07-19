# Engeto_Project_5_PowerBI

## Popis projektu

Tento Power BI projekt analyzuje data z oblasti prodeje, zisku a zákaznického servisu společnosti v období let 2014–2017.  
Cílem bylo vytvořit interaktivní vizuální report, který poskytne klíčový přehled o výkonu firmy, a zároveň umožní hlubší analýzu jednotlivých částí – produktů, segmentů, regionů a reklamací.

## Zadání projektu
Zadáním bylo vytvořit projekt v Power BI s náslejucími parametry:

- Rozsah 2-5 stránekPoužití minimálně 5 různých typů vizuálů
- Filtrování (primárně) pomocí průřezů/slicerů
- Využití interaktivních prvků jako jsou záložky, navigace po stranách, odkazy na webové stránky
- Propojení několika (2+) datových tabulek, buď přes vazby v rámci Power BI nebo přes propojení v Power Query
- Použití vytvořené hierarchie o alespoň dvou úrovních (nepovinné)
- Vytvoření alespoň 1 measure (metrika/míra) a 1 kalkulovaného sloupce/tabulky
- Grafická úprava použitých vizuálů, zvolení správných typů vizuálů a vizuálně přívětivý výsledný report


## Použité datové zdroje

- **Datová sada:** [Superstore Sales Dataset – Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)  
- **Načtené tabulky:**  
  - `Orders` – podrobnosti o objednávkách (datum, tržby, zisk, region atd.)  
  - `Returns` – informace o vrácených objednávkách  
  - `People` – obchodní zástupci přiřazení k regionům  


## ⚙Zpracování a model

### Relace:
- `Orders[Order ID]` → `Returns[Order ID]`
- `Orders[Region]` → `People[Region]` 
- Vytvořená pomocná tabulka `UniqueOrders` (unikátní objednávky s datem) pro analýzu v čase

### Vytvořené výpočty:
- **Measures (míry):**
  - `% reklamací`
  - `AVG_Profit_per_Order`
  - `Margin (%)` – marže v procentech  
- **Kalkulované sloupce:**
  - Měsíc a rok objednávky (pro vizualizaci)
  - Den v týdnu
  - Průměrná doba dodání (dny mezi objednáním a odesláním)


## Struktura reportu (5 stránek)

### 1. **Klíčové prodeje**
- KPI boxy: celkové tržby, zisk, počet objednávek, % reklamací
- Top 10 států podle tržeb, Vývoj tržeb v čase
- Průřezy: rok, region, segment, obchodní zástupce

### 2. **Prodeje v čase**
- Kombinovaný graf: vývoj tržeb a počtu objednávek v čase
- Tržby podle dne v týdnu
- Průřezy: rok, čtvrtletí, měsíc, segment, kategorie, region, obchodní zástupce

### 3. **Ziskovost**
- KPI boxy: celkový zisk, marže (%), průměrný zisk na objednávku
- Zisk v čase (čárový graf)
- Marže podle segmentu, regionu nebo kategorie (možnost přepínat přes záložky)
- Průřezy: rok, čtvrtletí, obchodní zástupce, region, segment, kategorie

### 4. **Produkty**
- Tabulka: TOP 10 produktů podle zisku
- Počet objednávek podle podkategorie (vodorovný graf)
- POčet prodaných kusů v segmentu
- Průřezy: rok, segment, obchodní zástupce

### 5. **Reklamace a dodání**
- KPI boxy: počet objednávek, počet reklamací, % reklamací, průměrná doba dodání
- % reklamací v čase (měsíční trend)
- Reklamace podle regionu nebo kategorie
- Průměrná doba dodání (z `Order Date` do `Ship Date`)
- Průřezy: rok, region, kategorie


## Cíle projektu (splněné požadavky)

✔️ Rozsah 5 stránek  
✔️ Použito více než 5 typů vizuálů  
✔️ Slicery pro filtraci dat  
✔️ Interaktivní prvky: přepínání mezi kategoriemi (záložky), případně navigace  
✔️ Propojení více datových tabulek pomocí vztahů  
✔️ Vytvoření měr a kalkulovaných sloupců/tabulek  
✔️ Grafická úprava vizuálů a jednotný styl reportu  
✔️ Přehlednost, použitelnost a vhodné typy vizualizací

