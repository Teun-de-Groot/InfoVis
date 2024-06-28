The impact van COVID-19 op de wereldhandel
Jasper Wormsbecher, 14953110
Doede Cerutti, 14948095
Teun de Groot, 14892499
Guido Chung, 15113248
Team number: F1

Introductie
De coronacrisis heeft een grote impact gehad op verschillende sectoren, zoals onderwijs, economie en gezondheidszorg. Deze situatie heeft ertoe geleid dat mensen zoveel mogelijk geïsoleerd moesten worden om de verspreiding van het virus te beperken.
De COVID-19 pandemie heeft de wereldhandel verstoord, wat gevolgen had voor import, export en economische stabiliteit in verschillende regio's en sectoren. Dit project onderzoekt de impact van de pandemie op de handel door trends, verschuivingen en herstel te analyseren. We verkennen meerdere perspectieven om een uitgebreid inzicht te geven in hoe de pandemie de dynamiek van de wereldhandel heeft beïnvloed.

Dataset en Preprocessing

1. Wereldhandelsdata (https://github.com/farhansadeed/Python-COVID-19-Trade-Impact-Data-Analysis) 
2. Covid-19 data (https://covid.ourworldindata.org/data/owid-covid-data.csv)

We hebben gebruikgemaakt van twee datasets, geselecteerd om zowel de wereldhandel als de COVID-19 crisis te analyseren. Hierbij hebben we ervoor gekozen om ons uitsluitend op wereldwijde gegevens te richten, waardoor we geen uitspraken kunnen doen over individuele landen.

Om de gegevens op te schonen, hebben we kolommen hernoemd en geherstructureerd voor samenvoeging. We hebben de kolommen handmatig geïnspecteerd en samengevoegd op basis van overeenkomende namen of inhoud. Tijdens dit proces hebben we meteen de niet-relevante kolommen verwijderd.


Hierna zijn de totaal 77 columns en samen 514232 rijen gereduceerd tot een dataset van 31 columns met 711 rijen. Voor sommige visualisaties worden de individuele datasets gebruikt.
Variable descriptions

Voor sommige visualisaties worden de individuele datasets gebruikt. 
De variabelen in de uiteindelijke dataset omvatten:

Continuous / Ratio variables: total_cases, new_cases, new_cases_smoothed, total_deaths,new_deaths, new_deaths_smoothed, total_cases_per_million,new_cases_per_million, new_cases_smoothed_per_million,total_deaths_per_million, new_deaths_per_million,new_deaths_smoothed_per_million, total_vaccinations, people_vaccinated, people_fully_vaccinated,total_boosters, new_vaccinations, new_vaccinations_smoothed,total_vaccinations_per_hundred, people_vaccinated_per_hundred,people_fully_vaccinated_per_hundred, total_boosters_per_hundred,new_vaccinations_smoothed_per_million,new_people_vaccinated_smoothed,new_people_vaccinated_smoothed_per_hundred, Value_x, Cumulative_x, Value_y, Cumulative_y, reproduction_rate
discrete / interval: ‘date’

De variabelen in de covid-19 dataset variabele:
discrete / nominal: iso_code, location
discrete / interval: date
continues / ratio: total_cases, new_cases, new_cases_smoothed, total_deaths, new_deaths, new_deaths_smoothed, total_cases_per_million, new_cases_per_million, new_cases_smoothed_per_million, total_deaths_per_million, new_deaths_per_million, new_deaths_smoothed_per_million, reproduction_rate, icu_patients, icu_patients_per_million, hosp_patients, hosp_patients_per_million, weekly_icu_admissions, weekly_icu_admissions_per_million, weekly_hosp_admissions, weekly_hosp_admissions_per_million, total_tests, new_tests, total_tests_per_thousand, new_tests_per_thousand,new_tests_smoothed, new_tests_smoothed_per_thousand, positive_rate, tests_per_case, tests_units, total_vaccinations, people_vaccinated, people_fully_vaccinated, total_boosters, new_vaccinations, new_vaccinations_smoothed, total_vaccinations_per_hundred, people_vaccinated_per_hundred, people_fully_vaccinated_per_hundred, total_boosters_per_hundred, new_vaccinations_smoothed_per_million, new_people_vaccinated_smoothed, new_people_vaccinated_smoothed_per_hundred, stringency_index, population_density, median_age, aged_65_older, aged_70_older, gdp_per_capita, extreme_poverty, cardiovasc_death_rate, diabetes_prevalence, female_smokers, male_smokers, handwashing_facilities, hospital_beds_per_thousand, life_expectancy, human_development_index, population, excess_mortality_cumulative_absolute, excess_mortality_cumulative, excess_mortality, excess_mortality_cumulative_per_million

De variabelen in de economische dataset variabele:
discrete / nominal: 'Direction'
discrete / interval: ‘date’
continues / ratio: 'Value', 'Cumulative'
De invloed van vaccinaties op de zorg en overheidsmaatregelen
Vaccinaties spelen een cruciale rol in de verbetering van de wereldgezondheid. Door het voorkomen van ernstige ziektes en het verminderen van de verspreiding van besmettelijke aandoeningen, dragen vaccinaties bij aan een algehele verbetering van de medische situatie wereldwijd.
Doden veroorzaakt door covid-19
Om te kunnen bepalen of de vaccinaties beter waren voor de wereld op medisch gebied moeten we eerst specificeren wat “goed” is. Hierbij gaan we analyseren of de vaccinaties ervoor gezorgd hebben dat er minder doden en totale gevallen waren.


We hebben ontdekt dat er een correlatie bestaat tussen vaccinaties en de totale hoeveelheid doden in de wereld. Wanneer de vaccinaties omhoog gaan, gaan de vaccinaties ook omhoog. Dit komt niet omdat vaccinaties doden veroorzaken. Maar omdat corona doden veroorzaakt en de vaccinatiegraad ook langzaam over tijd omhoog gaat. Hierdoor heb je een correlatie, maar geen causaliteit. Wanneer de vaccinatiegraad omhoog gaat, dan zijn er minder nieuwe doden, omdat er een zware negatieve correlatie is tussen de vaccinatiegraad en de hoeveelheid nieuwe doden. 

Verder vonden kijken we naar de stringency index, dit is een samengestelde maatstaf die de strengheid van overheidsmaatregelen in reactie op de COVID-19-pandemie kwantificeert. Deze index maakt deel uit van de Oxford COVID-19 Government Response Tracker (OxCGRT) en wordt berekend met de volgende formule:

De index wordt berekend aan de hand van de volgende maatregelen:
Sluiting van scholen
Sluiting van werkplekken
Annulering van publieke evenementen
Beperkingen op bijeenkomsten
Sluiting van openbaar vervoer
Blijf-thuis voorschriften
Beperkingen op interne verplaatsingen
Internationale reisbeperkingen
Publieke voorlichtingscampagnes
De index varieert van 0 tot 100, waarbij hogere waarden een strengere overheidsreactie aangeven.
In het kort, de hoeveelheid maatregelen die een overheid nam om de corona crisis te beteugelen. Hierdoor kunnen we het beleid van de overheden meenemen in de conclusie. We kunnen zeggen dat de vaccinatie 1 van de factoren is geweest die ervoor heeft gezorgd dat minder doden zijn gevallen, omdat tijd of natuurlijke blootstelling aan het virus ook een factor kan zijn.


Nieuwe gevallen
Verder zouden we graag willen weten hoe de vaccinatiegraad de hoeveelheid corona gevallen beïnvloed. 
We vinden geen correlatie tussen de vaccinatiegraad en nieuwe gevallen van corona. Hierdoor kunnen we niet vaststellen dat een vaccinatie helpt bij het verminderen van de verspreiding van corona. Zoals wij het hier zien, heb je een vrij constante hoeveelheid mensen die ziek worden van het virus, ook al zien we wel wanneer de vaccinatiegraad hoger ligt dat er een stijging van nieuwe corona gevallen is. Hier hebben wij geen goede verklaring voor. Maar we kunnen speculeren dat dit een geval is van toeval. Verder is het ook belangrijk om dit te melden, want dan weten we in de toekomst wat een vaccinatie wel en niet bestrijdt.

We kunnen deze 2 argumenten samen zetten en dan krijgen we de volgende figuur

Hierin is te zien, dat een groot deel van de bevolking volgens onze data corona heeft gekregen. Dit kan komen omdat het in bepaalde delen van de wereld het moeilijk is om te bepalen hoeveel corona gevallen er daadwerkelijk aanwezig zijn. Wat we wel hieruit kunnen concluderen is dat er maar een kleine kans is om van corona dood te gaan. Dit is niet te zien in het figuurtje aangezien het percentage zo klein is. Het onderdeel "total deaths" heeft maar een grootte van 0.08%.
De invloed van vaccinaties op de economie
De invloed van vaccinaties op de economie is aanzienlijk en veelzijdig. Vaccinaties spelen een belangrijke rol in het bevorderen van economische stabiliteit en groei wereldwijd.
Handelsactiviteit
In 2021 zien we een significante toename in het aantal vaccinaties. Dit valt samen met een herstellende trend in zowel de import- als exportwaarden, die in 2020 een dip vertonen. Deze gelijktijdige beweging suggereert een correlatie tussen het aantal vaccinaties en het herstel van de handelsactiviteiten.

De stijging van het aantal vaccinaties zou hebben kunnen bijdragen aan het heropenen van economieën, wat mogelijk resulteerde in verhoogde economische activiteit. Dit herstel lijkt weerspiegeld te worden in de import- en exportsectoren, zoals te zien is in de grafiek. Naarmate de bevolking gevaccineerd werd, nam wellicht het vertrouwen van bedrijven en consumenten toe, wat mogelijk heeft bijgedragen aan een toename van de handelsactiviteiten.


Overheidsmaatregelen
Het is bekend (Amador et al., 2023) dat beleidsmaatregelen zoals lockdowns en reisbeperkingen, gemeten door de Stringency Index, een aanzienlijke invloed hebben op internationale handelsstromen, waaronder import en export. Een analyse van de dataset toont een duidelijk verband tussen deze beleidsmaatregelen en schommelingen in import- en export waarden. De grafiek toont de import- en export waarden over de tijd, evenals de Global Stringency Index.

Tijdens periodes waarin de Stringency Index stijgt, wat wijst op strikte maatregelen zoals lockdowns, zien we een duidelijke daling in zowel import- als export waarden. Dit komt doordat strenge maatregelen leiden tot verstoringen in de toeleveringsketen. Bijvoorbeeld, tijdens de COVID-19-pandemie in 2020 en begin 2021, is er een duidelijke afname in handelsactiviteiten zichtbaar.
Naarmate de Stringency Index daalt en maatregelen versoepelen, zien we een herstel in zowel import- als exportwaarden. Dit herstel weerspiegelt de hernieuwde economische activiteit en hervatting van internationale handel na het terugdraaien van overheidsinmenging.
Feedback en Reflectie
Op 25 juni 2024 is onze groep bijeengekomen op Science Park voor het feedbackmoment. Hier zijn een aantal zwakke punten van het project aangekaart.

Ten tijde van het feedbackmoment maakten we nog enkel gebruik van lijngrafieken, het advies was dan ook meer verschillende soorten grafieken te gebruiken. Hierdoor komt de boodschap die we over willen brengen met de data beter tot zijn recht.
Alle grafieken waar we gebruik van maakten hadden variabelen op de y-as en tijd op de x-as. Het advies was andere variabelen dan enkel de tijd op de x-as te gebruiken.
Twee plots die los van elkaar staan en beiden tijd op de x-as hebben, kunnen niet zomaar met elkaar vergeleken worden. Oftewel voorzichtiger taalgebruik; plots geven enkel correlaties weer. We concludeerden bijvoorbeeld dat er een causaal verband is tussen een hogere vaccinatiegraad en een kleinere stringency index hoewel dit enkel correlatie is.
Een van de grafieken waar we gebruik van maakten gaf cumulatief de covid-19 cases van elk land in de wereld apart weer, met een dikkere lijn om de gemiddelde trend aan te geven. Dit was erg onoverzichtelijk.

Reflecterend op het verloop van het project zijn er twee dingen waar we op vastliepen.

Ten eerste hebben we erg geworsteld met het vinden van een goed onderwerp. Dit is het gevolg van gebrekkig onderzoek naar correlaties tussen de datasets waar we destijds gebruik van maakten. Om deze reden gaat onze final delivery over een ander onderwerp dan onze proposal.

Het tweede punt is dat we erg inefficiënt hebben gewerkt in verband met miscommunicatie. Meerdere keren is het voorgekomen dat men dubbel werk heeft verricht, zoals het zoeken naar correlaties of het maken van plots.



Werkverdeling
Guido
Guido heeft ervoor gezorgd dat de teksten goed leesbaar zijn. Verder heeft hij een van de perspectieven, de samenvatting en het stuk over de dataset en de preprocessing geschreven. Ook heeft hij aan de introductie gewerkt.

Jasper
Jasper heeft het grootste deel van het coderen gedaan, zoals preprocessing, het vinden van correlaties en het maken van de plots waar gebruik van is gemaakt in de definitieve versie van het project. Verder heeft hij het verhaal rondom de data en plots in goede banen geleid en de introductie met Guido geschreven. Ook heeft hij het project gepresenteerd tijdens het feedbackmoment. Jasper hield de planning bij en had goed overzicht over de te verdelen taken.

Doede
Doede heeft een grootste deel van de argumenten uitgewerkt en geholpen bij het bedenken van plots die deze argumenten ondersteunen. Ook heeft hij de feedback bijgehouden.
Doede heeft net als Jasper gewerkt aan het vinden van correlaties en het maken van plots, dit is onderdeel van het dubbele werk dat genoemd wordt in de reflectie.

Teun
Teun heeft aan de argumenten en de globale verhaallijn gewerkt. Verder heeft hij het stukje feedback en reflectie en deze work distribution geschreven.
Teun heeft net als Doede feedback bijgehouden tijdens het feedbackmoment en aan het begin van het project dubbel werk verricht met betrekking tot het zoeken naar correlaties en het maken van plots.

Samenvatting
De corona pandemie heeft wereldwijd een aanzienlijke invloed gehad op zowel de sociale als de economische sectoren. Om deze impact te meten, is er veel data verzameld en in ons onderzoek hebben we ons gericht op vaccinaties, import/export en de stringency index. Uit onze analyse bleek dat vaccinaties mogelijk hebben bijgedragen aan herstel op zowel medisch als economisch gebied. Hoewel er geen direct verband werd gevonden tussen de vaccinatiegraad en het aantal nieuwe corona gevallen, was er economisch herstel zichtbaar in de import- en exportwaarden naarmate de vaccinatiegraad toenam en de overheidsmaatregelen versoepelden. Verdere studie is echter nodig om deze bevindingen te bevestigen en om een dieper inzicht te krijgen in de complexiteit van de relatie tussen vaccinaties, economische activiteit en beleidsmaatregelen gedurende de pandemie.

Bronnen
Centraal Bureau voor de Statistiek. (2023). More strikes but fewer strikers in 2022. Statistics Netherlands. https://www.cbs.nl/en-gb/news/2023/18/more-strikes-but-fewer-strikers-in-2022
https://www.ecdc.europa.eu/en/covid-19/vaccines-roll-out

COVID-19 vaccination. (z.d.). RIVM. https://www.rivm.nl/en/covid-19-vaccination


Amador, J., Gouveia, C. M., & Pimenta, A. C. (2023). COVID-19, lockdowns and international trade: evidence from firm-level data. Empirical Economics, 65(5), 2427–2466. https://doi.org/10.1007/s00181-023-02421-x
