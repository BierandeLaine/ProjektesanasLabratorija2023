# Programmatūras apraksts

Lietotājs atver pārlūku un autentificējas sistēmā ar lietotājvārdu un paroli. Pēc veiksmīgas autentifikācijas lietotājs tiek novirzīts uz lapu,
kurā var izvēlēties divas opcijas- pārlūkot iepriekšējos ražošanas plānus vai izveidot jaunu ražošanas plānu. Ja tiek veikta izvēle- pārlūkot 
iepriekšējos, tad nospiežot attiecīgo pogu, lietotājs tiek aizvests uz lapu, kurā ir redzami visi iepriekšējie ražošanas plāni. Savukārt, ja 
lietotājs izvēlas otru opciju- Jauns ražošanas plāns, tad lietotājs tiek aizvests uz lapu, kurā tiek piedāvātās izvēlēs iespējas, ievadīt 
paramterus (Grāmata, grāmataps tips- citie/mīkstie vāki un apjoms), lai tiktu izvadīta vidējā peļņa. Lietotājs var izvēlēties visas izvēlē 
pieejamās grāmatas un tiek izvadīti dati tabulas veidā, par izvēlēto grāmatu, grāmatas tipu, apjomu un peļņu un tādā veidā var lietotājs var
salīdzināt iegūtos rezultātus un noteikt, no kādām grāmātām un kāda apjoma, tik gūta lielākā peļņa. 
	Lai aprēķinātu vidējo peļņu pamatojoties uz lietotāja izvēli no HTML formas un datu bāzes datus, tiek izmantots Python kopā ar 
Flask bibliotēku, lai sazinātos ar datu bāzi un attiecīgi attēlotu rezultātu HTML lapā. Flask servera kods, lai saņemtu izvēli no formas un
aprēķinātu vidējo peļņu, pamatojoties uz datu bāzes informāciju, tiek ierakstīts app.py failā, kodā ir pievienota funkcija calculate_average_profit
vidējās peļņas aprēķinam. Līdz ar to, kad lietotājs iesniedz formu, aprēķinātā vidējā peļņa no datu bāzes, tiek izvadīta HTML lapā. Tiek pievienots
ar script.js fails, lai attēlotu veiktās izvēles HTML lapā. Scripta faila kods veic šādas darbības: Kad lietotājs noklikšķina uz "Aprēķināt vidējo peļņu" 
pogas, tas izsūta POST pieprasījumu uz serveri ar izvēlētajām vērtībām. Kad serveris atgriež atbildi ar vidējo peļņu, JavaScript izveido jaunu rindu 
tabulā (<tr>) un pievieno šajā rindā šo informāciju - grāmatas nosaukums, vāka tips, apjoms un vidējā peļņa vērtība.
