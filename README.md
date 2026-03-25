# Cobol-DB2-JCL-MT940-en-camt.053

## eigen project
## MT940
Het doel dat ik mij gesteld had, was het maken van een job met twee programmas voor het verwerken van een electronisch rekeningafschrift MT940 dat een fictieve verzekeringsmaatschappij dagelijks van PostFinance ontvangt. Het dossier bevat:
1. **Cobol programma BNQ0001R**: verwrking van een SWIFT bestand **MT940** (rekeningafschrift). Output: een tussenbestand, controle- en foutlijst. Lees-toegang tot **DB2**
2. **Cobol programma BNQ0002W**: update van 2 **DB2** tabellen via **embedded SQL**. Invoer: tussenbestand, gesorteerd. Uitvoer: controle- en foutlijst.
3. **Analyses**, broncode, compilaties **Cobol**, **SQL**, **JCL**, plus de **testresultaten**.

## camt.053
Omdat het formaat MT940 niet meer ondersteund wordt sinds november 2025, heb ik ook het skelet van een programma geschreven, dat het  wel ondersteunde  formaat **camt.053 (XML)** verwerkt. Het dossier bevat:
1. **Cobol programme BNQ0003**, een snelle opzet zonder lijsten of controles, die zich beperkt tot het ontcijferen van het **XML-bericht** om dezelfde gegevens als de BNQ0001R door te kunnen sturen naar BNQ0002W via een tussenbestand.  **BNQ0002W verwerkt zonder problemen de gegevens van BNQ0003**.
2. Snelle analyse, die zich beperkt tot een mapping en enkele opmerkingen.

## Dankwoord
Ik heb dit project kunnen realiseren via de toegang tot een mainframe **IBM z/OS** van het IBM Open Mainframe Project, gebruik makend van **VS-Code** en de extensie **ZOWE**.
*Ik dank IBM hartelijk voor deze toegang.*
