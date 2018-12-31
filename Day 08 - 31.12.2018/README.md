# Step 1 - Create DB + Collections with data
* Create in mongo DB a new DB named `Universities`.   
Command:
```javascript
use Universities
```
* Crearte a new collection named `countryInfo`, and insert into it the following documnts:


```json
[{"name":"Israel","topLevelDomain":[".il"],"alpha2Code":"IL","alpha3Code":"ISR","callingCodes":["972"],"capital":"Jerusalem","altSpellings":["IL","State of Israel","Medīnat Yisrā'el"],"region":"Asia","subregion":"Western Asia","population":8527400,"latlng":[31.5,34.75],"demonym":"Israeli","area":20770.0,"gini":39.2,"timezones":["UTC+02:00"],"borders":["EGY","JOR","LBN","SYR"],"nativeName":"יִשְׂרָאֵל","numericCode":"376","currencies":[{"code":"ILS","name":"Israeli new shekel","symbol":"₪"}],"languages":[{"iso639_1":"he","iso639_2":"heb","name":"Hebrew (modern)","nativeName":"עברית"},{"iso639_1":"ar","iso639_2":"ara","name":"Arabic","nativeName":"العربية"}],"flag":"https://restcountries.eu/data/isr.svg","regionalBlocs":[],"cioc":"ISR"},{"name":"Germany","topLevelDomain":[".de"],"alpha2Code":"DE","alpha3Code":"DEU","callingCodes":["49"],"capital":"Berlin","altSpellings":["DE","Federal Republic of Germany","Bundesrepublik Deutschland"],"region":"Europe","subregion":"Western Europe","population":81770900,"latlng":[51.0,9.0],"demonym":"German","area":357114.0,"gini":28.3,"timezones":["UTC+01:00"],"borders":["AUT","BEL","CZE","DNK","FRA","LUX","NLD","POL","CHE"],"nativeName":"Deutschland","numericCode":"276","currencies":[{"code":"EUR","name":"Euro","symbol":"€"}],"languages":[{"iso639_1":"de","iso639_2":"deu","name":"German","nativeName":"Deutsch"}],"flag":"https://restcountries.eu/data/deu.svg","regionalBlocs":[{"acronym":"EU","name":"European Union","otherAcronyms":[],"otherNames":[]}],"cioc":"GER"}]
```

first Command:
```javascript
db.createCollection("countryInfo")
```
result:
```
{ "ok" : 1 }
```

second Command:
```javascript
db.countryInfo.insert(
[
    {
        "name": "Israel",
        "topLevelDomain": [
            ".il"
        ],
        "alpha2Code": "IL",
        "alpha3Code": "ISR",
        "callingCodes": [
            "972"
        ],
        "capital": "Jerusalem",
        "altSpellings": [
            "IL",
            "State of Israel",
            "Medīnat Yisrā'el"
        ],
        "region": "Asia",
        "subregion": "Western Asia",
        "population": 8527400,
        "latlng": [
            31.5,
            34.75
        ],
        "demonym": "Israeli",
        "area": 20770.0,
        "gini": 39.2,
        "timezones": [
            "UTC+02:00"
        ],
        "borders": [
            "EGY",
            "JOR",
            "LBN",
            "SYR"
        ],
        "nativeName": "יִשְׂרָאֵל",
        "numericCode": "376",
        "currencies": [
            {
                "code": "ILS",
                "name": "Israeli new shekel",
                "symbol": "₪"
            }
        ],
        "languages": [
            {
                "iso639_1": "he",
                "iso639_2": "heb",
                "name": "Hebrew (modern)",
                "nativeName": "עברית"
            },
            {
                "iso639_1": "ar",
                "iso639_2": "ara",
                "name": "Arabic",
                "nativeName": "العربية"
            }
        ],
        "flag": "https://restcountries.eu/data/isr.svg",
        "regionalBlocs": [],
        "cioc": "ISR"
    },
    {
        "name": "Germany",
        "topLevelDomain": [
            ".de"
        ],
        "alpha2Code": "DE",
        "alpha3Code": "DEU",
        "callingCodes": [
            "49"
        ],
        "capital": "Berlin",
        "altSpellings": [
            "DE",
            "Federal Republic of Germany",
            "Bundesrepublik Deutschland"
        ],
        "region": "Europe",
        "subregion": "Western Europe",
        "population": 81770900,
        "latlng": [
            51.0,
            9.0
        ],
        "demonym": "German",
        "area": 357114.0,
        "gini": 28.3,
        "timezones": [
            "UTC+01:00"
        ],
        "borders": [
            "AUT",
            "BEL",
            "CZE",
            "DNK",
            "FRA",
            "LUX",
            "NLD",
            "POL",
            "CHE"
        ],
        "nativeName": "Deutschland",
        "numericCode": "276",
        "currencies": [
            {
                "code": "EUR",
                "name": "Euro",
                "symbol": "€"
            }
        ],
        "languages": [
            {
                "iso639_1": "de",
                "iso639_2": "deu",
                "name": "German",
                "nativeName": "Deutsch"
            }
        ],
        "flag": "https://restcountries.eu/data/deu.svg",
        "regionalBlocs": [
            {
                "acronym": "EU",
                "name": "European Union",
                "otherAcronyms": [],
                "otherNames": []
            }
        ],
        "cioc": "GER"
    }
]
)
```
result:
```
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 2,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
```
* Crearte a new collection named `uniInfo`, and insert into it the following documnts:
```json
[{"web_pages": ["http://www.afeka.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["afeka.ac.il"], "name": "Afeka Tel Aviv Academic College of Engineering"}, {"web_pages": ["http://www.ariel.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["ariel.ac.il"], "name": "Ariel University Center of Samaria"}, {"web_pages": ["http://www.ash-college.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["ash-college.ac.il"], "name": "Ashkelon Academic College"}, {"web_pages": ["http://www.bezalel.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["bezalel.ac.il"], "name": "Bezalel Academy of Art and Design"}, {"web_pages": ["http://www.bgu.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["bgu.ac.il"], "name": "Ben-Gurion University of the Negev"}, {"web_pages": ["http://www.biu.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["biu.ac.il"], "name": "Bar-Ilan University"}, {"web_pages": ["http://www.clb.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["clb.ac.il"], "name": "Acdemic Center for Law and Business"}, {"web_pages": ["http://www.colman.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["colman.ac.il"], "name": "College of Management"}, {"web_pages": ["http://www.galilcol.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["galilcol.ac.il"], "name": "Galillee College"}, {"web_pages": ["http://www.haifa.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["haifa.ac.il"], "name": "University of Haifa"}, {"web_pages": ["http://www.huji.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["huji.ac.il"], "name": "Hebrew University of Jerusalem"}, {"web_pages": ["http://www.idc.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["idc.ac.il"], "name": "The Interdisciplinary Center Herzliya"}, {"web_pages": ["http://www.juc.edu/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["juc.edu"], "name": "Jerusalem University College"}, {"web_pages": ["http://www.openu.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["openu.ac.il"], "name": "Open University of Israel"}, {"web_pages": ["http://rbni.technion.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["rbni.technion.ac.il"], "name": "Russell Berrie Nanotechnology Institute"}, {"web_pages": ["http://www.sce.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["sce.ac.il"], "name": "Sami Shamoon College of Engineering"}, {"web_pages": ["http://www.shenkar.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["shenkar.ac.il"], "name": "Shenkar School of Engineering & Design"}, {"web_pages": ["http://www.tau.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["tau.ac.il"], "name": "Tel Aviv University"}, {"web_pages": ["http://www.technion.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["technion.ac.il"], "name": "Technion - Israel Institute of Technology"}, {"web_pages": ["http://www.weizmann.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["weizmann.ac.il"], "name": "Weizmann Institute of Science"}, {"web_pages": ["http://www.wgalil.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["wgalil.ac.il"], "name": "Western Galilee College"}, {"web_pages": ["http://www.yvc.ac.il/"], "alpha_two_code": "IL",  "country": "Israel", "domains": ["yvc.ac.il"], "name": "Emeq Yizrael College"},{"web_pages": ["http://www.akad.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["akad.de"], "name": "AKAD Hochschulen f\u00fcr Berufst\u00e4tige, Fachhochschule Leipzig"}, {"web_pages": ["http://www.akad.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["akad.de"], "name": "Hochschule f\u00fcr Berufst\u00e4tige Rendsburg"}, {"web_pages": ["http://www.asfh-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["asfh-berlin.de"], "name": "Alice-Salomon-Fachhochschule f\u00fcr Sozialarbeit und Sozialp\u00e4dagogik Berlin"}, {"web_pages": ["http://www.augustana.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["augustana.de"], "name": "Augustana Hochschule Neuendettelsau"}, {"web_pages": ["http://www.bethel.de/kiho/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["bethel.de"], "name": "Kirchliche Hochschule Bethel"}, {"web_pages": ["http://www.bits-iserlohn.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["bits-iserlohn.de"], "name": "BiTS - Business and Information Technology School gGmbH"}, {"web_pages": ["http://www.cbs.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["cbs.de"], "name": "Cologne Business School"}, {"web_pages": ["http://www.dhbw.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["dhbw.de"], "name": "Duale Hochschule Baden-W\u00fcrttemberg"}, {"web_pages": ["http://www.dhv-speyer.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["dhv-speyer.de"], "name": "Deutsche Hochschule f\u00fcr Verwaltungswissenschaften Speyer"}, {"web_pages": ["http://www.diploma.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["diploma.de"], "name": "DIPLOMA-Fachhochschule \u00d6lsnitz/Vogtland"}, {"web_pages": ["http://www.diploma.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["diploma.de"], "name": "Fachhochschule Nordhessen"}, {"web_pages": ["http://www.dshs-koeln.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["dshs-koeln.de"], "name": "Deutsche Sporthochschule K\u00f6ln"}, {"web_pages": ["http://www.eap.net/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["eap.net"], "name": "E.A.P. Europ\u00e4ische Wirtschaftshochschule Berlin"}, {"web_pages": ["http://www.eba-muenchen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["eba-muenchen.de"], "name": "Europ\u00e4ische Betriebswirtschafts-Akademie"}, {"web_pages": ["http://www.ebs.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ebs.de"], "name": "European Business School Schlo\u00df Reichartshausen"}, {"web_pages": ["http://www.ecla.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ecla.de"], "name": "European College of Liberal Arts"}, {"web_pages": ["http://www.efh-bochum.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["efh-bochum.de"], "name": "Evangelische Fachhochschule Rheinland-Westfalen-Lippe"}, {"web_pages": ["https://www.eh-darmstadt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["eh-darmstadt.de"], "name": "Evangelische Fachhochschule Darmstadt"}, {"web_pages": ["http://www.efh-freiburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["efh-freiburg.de"], "name": "Evangelische Fachhochschule Freiburg, Hochschule f\u00fcr Soziale Arbeit, Diakonie und Religionsp\u00e4dagogik"}, {"web_pages": ["http://www.efh-hannover.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["efh-hannover.de"], "name": "Evangelische Fachhochschule Hannover"}, {"web_pages": ["http://www.efhlu.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["efhlu.de"], "name": "Evangelische Fachhochschule Ludwigshafen Hochschule f\u00fcr Sozial- und Gesundheitswesen"}, {"web_pages": ["http://www.efh-reutlingen-ludwigsburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["efh-reutlingen-ludwigsburg.de"], "name": "Evangelische Fachhochschule Reutlingen-Ludwigsburg, Hochschule f\u00fcr Soziale Arbeit, Religionsp\u00e4dagogik und Diakonie"}, {"web_pages": ["http://www.ehs-dresden.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ehs-dresden.de"], "name": "Evangelische Hochschule f\u00fcr Soziale Arbeit Dresden (FH)"}, {"web_pages": ["http://www.ems-mainz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ems-mainz.de"], "name": "European Management School"}, {"web_pages": ["http://www.eufh.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["eufh.de"], "name": "Europ\u00e4ische Fachhochschule"}, {"web_pages": ["http://www.euv-frankfurt-o.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["euv-frankfurt-o.de"], "name": "Europa-Universit\u00e4t Viadrina Frankfurt (Oder)"}, {"web_pages": ["http://www.evfh-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["evfh-berlin.de"], "name": "Evangelische Fachhochschule Berlin, Fachhochschule f\u00fcr Sozialarbeit und Sozialp\u00e4dagogik"}, {"web_pages": ["http://www.evfh-nuernberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["evfh-nuernberg.de"], "name": "Evangelische Fachhochschule N\u00fcrnberg"}, {"web_pages": ["http://www.fern-fh.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fern-fh.de"], "name": "Fern-Fachhochschule Hamburg"}, {"web_pages": ["http://www.fernuni-hagen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fernuni-hagen.de"], "name": "Fernuniversit\u00e4t Gesamthochschule Hagen"}, {"web_pages": ["http://www.fh-aachen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-aachen.de"], "name": "Fachhochschule Aachen"}, {"web_pages": ["http://www.fh-aschaffenburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-aschaffenburg.de"], "name": "Fachhochschule Aschaffenburg"}, {"web_pages": ["http://www.fh-augsburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-augsburg.de"], "name": "Fachhochschule Augsburg"}, {"web_pages": ["http://www.fh-bad-honnef.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-bad-honnef.de"], "name": "Internationale Fachhochschule Bad Honnef"}, {"web_pages": ["http://www.fh-biberach.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-biberach.de"], "name": "Fachhochschule Biberach, Hochschule f\u00fcr Bauwesen und Wirtschaft"}, {"web_pages": ["http://www.fh-bielefeld.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-bielefeld.de"], "name": "Fachhochschule Bielefeld"}, {"web_pages": ["http://www.fh-bingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-bingen.de"], "name": "Fachhochschule Bingen"}, {"web_pages": ["http://www.fh-bochum.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-bochum.de"], "name": "Fachhochschule Bochum"}, {"web_pages": ["http://www.hochschule-bonn-rhein-sieg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hochschule-bonn-rhein-sieg.de", "h-brs.de"], "name": "Hochschule Bonn-Rhein-Sieg"}, {"web_pages": ["http://www.fh-brandenburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-brandenburg.de"], "name": "Fachhochschule Brandenburg"}, {"web_pages": ["http://www.th-brandenburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["th-brandenburg.de"], "name": "Technische Hochschule Brandenburg"}, {"web_pages": ["http://www.th-deg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["th-deg.de"], "name": "Technische Hochschule Deggendorf"}, {"web_pages": ["http://www.fh-dortmund.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-dortmund.de"], "name": "Fachhochschule Dortmund"}, {"web_pages": ["http://www.hs-duesseldorf.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-duesseldorf.de"], "name": "Hochschule D\u00fcsseldorf"}, {"web_pages": ["http://www.fhdw.bib.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhdw.bib.de"], "name": "Fachhochschule f\u00fcr die Wirtschaft"}, {"web_pages": ["http://www.fhdw.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhdw.de"], "name": "Fachhochschule der Wirtschaft"}, {"web_pages": ["http://www.fh-eberswalde.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-eberswalde.de"], "name": "Fachhochschule Eberswalde"}, {"web_pages": ["http://www.fh-erfurt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-erfurt.de"], "name": "Fachhochschule Erfurt"}, {"web_pages": ["http://www.fh-flensburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-flensburg.de"], "name": "Fachhochschule Flensburg"}, {"web_pages": ["http://www.fh-frankfurt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-frankfurt.de"], "name": "Fachhochschule Frankfurt am Main"}, {"web_pages": ["http://www.fh-fresenius.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-fresenius.de"], "name": "Europa Fachhochschule Fresenius"}, {"web_pages": ["http://www.fh-furtwangen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-furtwangen.de"], "name": "Fachhochschule Furtwangen, Hochschule f\u00fcr Technik und Wirtschaft"}, {"web_pages": ["http://www.fh-gelsenkirchen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-gelsenkirchen.de"], "name": "Fachhochschule Gelsenkirchen"}, {"web_pages": ["http://www.fh-giessen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-giessen.de"], "name": "Fachhochschule Gie\u00dfen-Friedberg"}, {"web_pages": ["http://www.fh-hamburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-hamburg.de"], "name": "Fachhochschule Hamburg"}, {"web_pages": ["http://www.fh-hannover.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-hannover.de"], "name": "Fachhochschule Hannover"}, {"web_pages": ["http://www.fh-heidelberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-heidelberg.de"], "name": "Fachhochschule Heidelberg"}, {"web_pages": ["http://www.fh-heilbronn.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-heilbronn.de"], "name": "Fachhochschule Heilbronn, Hochschule f\u00fcr Technik und Wirtschaft"}, {"web_pages": ["http://www.fh-hildesheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-hildesheim.de"], "name": "Fachhochschule Hildesheim/Holzminden/G\u00f6ttingen, Hochschule f\u00fcr angewandte Wissenschaft und Kunst"}, {"web_pages": ["http://www.fh-hof.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-hof.de"], "name": "Fachhochschule Hof"}, {"web_pages": ["http://www.fh-ingolstadt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-ingolstadt.de"], "name": "Fachhochschule Ingolstadt"}, {"web_pages": ["http://www.fh-isny.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-isny.de"], "name": "Fachhochschule und Berufskollegs NTA, Prof.Dr. Gr\u00fcbler gemein. GmbH"}, {"web_pages": ["http://www.fh-jena.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-jena.de"], "name": "Fachhochschule Jena"}, {"web_pages": ["http://www.fh-karlsruhe.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-karlsruhe.de"], "name": "Fachhochschule Karlsruhe, Hochschule f\u00fcr Technik"}, {"web_pages": ["http://www.fh-Kempten.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-Kempten.de"], "name": "Fachhochschule Kempten, Hochschule f\u00fcr Technik und Wirtschaft"}, {"web_pages": ["http://www.fh-kiel.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-kiel.de"], "name": "Fachhochschule Kiel"}, {"web_pages": ["http://www.fh-kl.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-kl.de"], "name": "Fachhochschule Kaiserslautern"}, {"web_pages": ["http://www.fh-koblenz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-koblenz.de"], "name": "Fachhochschule Koblenz"}, {"web_pages": ["http://www.fh-koeln.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-koeln.de"], "name": "Fachhochschule K\u00f6ln"}, {"web_pages": ["http://www.fh-konstanz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-konstanz.de"], "name": "Fachhochschule Konstanz, Hochschule f\u00fcr Technik, Wirtschaft und Gestaltung"}, {"web_pages": ["http://www.fhkt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhkt.de"], "name": "Staatlich anerkannte Fachhochschule f\u00fcr Kunsttherapie"}, {"web_pages": ["http://www.fh-landshut.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-landshut.de"], "name": "Fachhochschule Landshut, Hochschule f\u00fcr Wirtschaft - Sozialwesen - Technik"}, {"web_pages": ["http://www.fh-lausitz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-lausitz.de"], "name": "Fachhochschule Lausitz"}, {"web_pages": ["http://www.fh-lippe.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-lippe.de"], "name": "Fachhochschule Lippe"}, {"web_pages": ["http://www.fh-ludwigshafen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-ludwigshafen.de"], "name": "Fachhochschule Ludwigshafen, Hochschule f\u00fcr Wirtschaft"}, {"web_pages": ["http://www.fh-luebeck.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-luebeck.de"], "name": "Fachhochschule L\u00fcbeck"}, {"web_pages": ["http://www.fh-mainz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-mainz.de"], "name": "Fachhochschule Mainz"}, {"web_pages": ["http://www.fh-mannheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-mannheim.de"], "name": "Fachhochschule Mannheim, Hochschule f\u00fcr Technik und Gestaltung"}, {"web_pages": ["http://www.fh-merseburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-merseburg.de"], "name": "Fachhochschule Merseburg"}, {"web_pages": ["http://www.fhm-mittelstand.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhm-mittelstand.de"], "name": "Fachhochschule des Mittelstandes (FHM)"}, {"web_pages": ["http://www.fh-muenchen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-muenchen.de"], "name": "Fachhochschule M\u00fcnchen"}, {"web_pages": ["http://www.hm.edu/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hm.edu"], "name": "Hochschule M\u00fcnchen"}, {"web_pages": ["http://www.fh-muenster.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-muenster.de"], "name": "Fachhochschule M\u00fcnster"}, {"web_pages": ["http://www.fh-nb.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-nb.de"], "name": "Fachhochschule Neubrandenburg"}, {"web_pages": ["http://www.hs-neu-ulm.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-neu-ulm.de"], "name": "Hochschule Neu-Ulm, Hochschule Neu-Ulm University of applied sciences"}, {"web_pages": ["http://www.fh-niederrhein.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-niederrhein.de"], "name": "Fachhochschule Niederrhein"}, {"web_pages": ["http://www.fhnon.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhnon.de"], "name": "Fachhochschule Nordostniedersachsen"}, {"web_pages": ["http://www.fh-nordhausen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-nordhausen.de"], "name": "Fachhochschule Nordhausen"}, {"web_pages": ["http://www.fh-nuernberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-nuernberg.de"], "name": "Georg-Simon-Ohm-Fachhochschule N\u00fcrnberg"}, {"web_pages": ["http://www.fh-nuertingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-nuertingen.de"], "name": "Fachhochschule N\u00fcrtingen, Hochschule f\u00fcr Wirtschaft, Landwirtschaft und Landespflege"}, {"web_pages": ["http://www.fhoebb.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhoebb.de"], "name": "Fachhochschule f\u00fcr das \u00f6ffentliche Bibliothekswesen Bonn"}, {"web_pages": ["http://www.fh-offenburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-offenburg.de"], "name": "Fachhochschule Offenburg, Hochschule f\u00fcr Technik und Wirtschaft"}, {"web_pages": ["http://www.fh-oow.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-oow.de"], "name": "Fachhochschule Oldenburg/Ostfriesland/Wilhelmshaven"}, {"web_pages": ["http://www.fh-osnabrueck.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-osnabrueck.de"], "name": "Fachhochschule Osnabr\u00fcck"}, {"web_pages": ["http://www.fh-ottersberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-ottersberg.de"], "name": "Freie Kunst-Studienst\u00e4tte Ottersberg"}, {"web_pages": ["http://www.fh-pforzheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-pforzheim.de"], "name": "Fachhochschule Pforzheim, Hochschule f\u00fcr Gestaltung, Technik und Wirtschaft"}, {"web_pages": ["http://www.fh-potsdam.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-potsdam.de"], "name": "Fachhochschule Potsdam"}, {"web_pages": ["http://www.fh-regensburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-regensburg.de"], "name": "Fachhochschule Regensburg"}, {"web_pages": ["http://www.fh-reutlingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-reutlingen.de"], "name": "Fachhochschule Reutlingen, Hochschule f\u00fcr Technik und Wirtschaft"}, {"web_pages": ["http://www.fh-riedlingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-riedlingen.de"], "name": "Deutsch-Ordens Fachhochschule Riedlingen, Hochschule f\u00fcr Wirtschaft"}, {"web_pages": ["http://www.fh-rosenheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-rosenheim.de"], "name": "Fachhochschule Rosenheim, Hochschule f\u00fcr Technik und Wirtschaft"}, {"web_pages": ["http://www.fh-rottenburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-rottenburg.de"], "name": "Fachhochschule Rottenburg, Hochschule f\u00fcr Forstwirtschaft"}, {"web_pages": ["http://www.fh-schmalkalden.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-schmalkalden.de"], "name": "Fachhochschule Schmalkalden"}, {"web_pages": ["http://www.fh-schwaebischhall.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-schwaebischhall.de"], "name": "Fachhochschule Schw\u00e4bisch Hall, Hochschule f\u00fcr Gestaltung"}, {"web_pages": ["http://www.fhs-mannheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhs-mannheim.de"], "name": "Fachhochschule Mannheim, Hochschule f\u00fcr Sozialwesen"}, {"web_pages": ["http://www.fhs-moritzburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhs-moritzburg.de"], "name": "Evangelische Fachhochschule f\u00fcr Religionsp\u00e4dagogik, und Gemeindediakonie Moritzburg"}, {"web_pages": ["http://www.fh-stralsund.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-stralsund.de"], "name": "Fachhochschule Stralsund"}, {"web_pages": ["http://www.fh-telekom-leipzig.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-telekom-leipzig.de"], "name": "Deutsche Telekom Fachhochschule Leipzig"}, {"web_pages": ["http://www.fh-trier.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-trier.de"], "name": "Fachhochschule Trier, Hochschule f\u00fcr Technik, Wirtschaft und Gestaltung"}, {"web_pages": ["http://www.fht-stuttgart.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fht-stuttgart.de"], "name": "Fachhochschule Stuttgart, Hochschule f\u00fcr Technik"}, {"web_pages": ["http://www.fhtw-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhtw-berlin.de"], "name": "Fachhochschule f\u00fcr Technik und Wirtschaft Berlin"}, {"web_pages": ["http://www.hs-ulm.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-ulm.de"], "name": "Hochschule Ulm, Hochschule f\u00fcr Angewandte Wissenschaft"}, {"web_pages": ["http://www.fhvr.berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhvr.berlin.de"], "name": "Fachhochschule f\u00fcr Verwaltung und Rechtspflege Berlin"}, {"web_pages": ["http://www.fhw-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhw-berlin.de"], "name": "Fachhochschule f\u00fcr Wirtschaft Berlin"}, {"web_pages": ["http://www.fh-wedel.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-wedel.de"], "name": "Fachhochschule Wedel"}, {"web_pages": ["http://www.fh-weihenstephan.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-weihenstephan.de"], "name": "Fachhochschule Weihenstephan"}, {"web_pages": ["http://www.fh-weingarten.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-weingarten.de"], "name": "Fachhochschule Ravensburg-Weingarten"}, {"web_pages": ["http://www.fh-westkueste.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-westkueste.de"], "name": "Fachhochschule Westk\u00fcste, Hochschule f\u00fcr Wirtschaft und Technik"}, {"web_pages": ["http://www.fh-wiesbaden.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-wiesbaden.de"], "name": "Fachhochschule Wiesbaden"}, {"web_pages": ["http://www.fh-wolfenbuettel.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-wolfenbuettel.de"], "name": "Fachhochschule Braunschweig/Wolfenb\u00fcttel"}, {"web_pages": ["http://www.fh-worms.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-worms.de"], "name": "Fachhochschule Worms"}, {"web_pages": ["http://www.fhwt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fhwt.de"], "name": "Private Fachhochschule f\u00fcr Wirtschaft und Technik Vechta/Diepholz"}, {"web_pages": ["http://www.fh-wuerzburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-wuerzburg.de"], "name": "Fachhochschule W\u00fcrzburg - Schweinfurt"}, {"web_pages": ["http://www.fh-zwickau.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fh-zwickau.de"], "name": "Wests\u00e4chsische Hochschule Zwickau (FH)"}, {"web_pages": ["http://www.fom.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fom.de"], "name": "Fachhochschule f\u00fcr Oekonomie und Management (FOM)"}, {"web_pages": ["http://www.fu-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["fu-berlin.de"], "name": "Freie Universit\u00e4t Berlin"}, {"web_pages": ["http://www.hanseuni.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hanseuni.de"], "name": "Private Hanseuniversit\u00e4t"}, {"web_pages": ["http://www.hcu-hamburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hcu-hamburg.de"], "name": "Hafencity Universit\u00e4t Hamburg"}, {"web_pages": ["http://www.hdm-stuttgart.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hdm-stuttgart.de"], "name": "Fachhochschule Stuttgart, Hochschule der Medien"}, {"web_pages": ["http://www.hertie-school.org/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hertie-school.org"], "name": "Hertie School of Governance"}, {"web_pages": ["http://www.hfb.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hfb.de"], "name": "Hochschule f\u00fcr Bankwirtschaft (HfB), Private Fachhochschule der Bankakademie"}, {"web_pages": ["http://www.hfg-gmuend.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hfg-gmuend.de"], "name": "Fachhochschule Schw\u00e4bisch Gm\u00fcnd, Hochschule f\u00fcr Gestaltung"}, {"web_pages": ["http://www.hfph.mwn.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hfph.mwn.de"], "name": "Hochschule f\u00fcr Philosophie M\u00fcnchen"}, {"web_pages": ["http://www.hfp.mhn.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hfp.mhn.de"], "name": "Hochschule f\u00fcr Politik (HFP)"}, {"web_pages": ["http://www.hhl.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hhl.de"], "name": "Handelshochschule Leipzig"}, {"web_pages": ["http://www.himh.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["himh.de"], "name": "Hochschule f\u00fcr Internationales Management"}, {"web_pages": ["http://www.hjs.uni-heidelberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hjs.uni-heidelberg.de"], "name": "Hochschule f\u00fcr J\u00fcdische Studien Heidelberg"}, {"web_pages": ["http://www.hs-albsig.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-albsig.de"], "name": "Hochschule Albstadt-Sigmaringen"}, {"web_pages": ["http://www.hs-anhalt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-anhalt.de"], "name": "Hochschule Anhalt (FH), Hochschule f\u00fcr angewandte Wissenschaften"}, {"web_pages": ["http://www.hs-bremen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-bremen.de"], "name": "Hochschule Bremen"}, {"web_pages": ["http://www.hs-bremerhaven.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-bremerhaven.de"], "name": "Hochschule Bremerhaven"}, {"web_pages": ["http://www.hs-coburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-coburg.de"], "name": "Hochschule Coburg"}, {"web_pages": ["https://www.h-da.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["h-da.de"], "name": "Hochschule Darmstadt"}, {"web_pages": ["http://www.hs-esslingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-esslingen.de"], "name": "Hochschule Esslingen"}, {"web_pages": ["http://www.hs-fulda.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-fulda.de"], "name": "Hochschule Fulda"}, {"web_pages": ["http://www.hs-harz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-harz.de"], "name": "Hochschule Harz, Hochschule f\u00fcr angewandte Wissenschaften (FH)"}, {"web_pages": ["http://www.hs-magdeburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-magdeburg.de"], "name": "Hochschule Magdeburg-Stendal (FH)"}, {"web_pages": ["http://www.hs-wismar.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-wismar.de"], "name": "Hochschule Wismar, Fachhochschule f\u00fcr Technik, Wirtschaft und Gestaltung"}, {"web_pages": ["http://www.hs-zigr.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hs-zigr.de"], "name": "Hochschule Zittau/G\u00f6rlitz (FH)"}, {"web_pages": ["http://www.htw-dresden.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["htw-dresden.de"], "name": "Hochschule f\u00fcr Technik und Wirtschaft Dresden (FH)"}, {"web_pages": ["http://www.htwk-leipzig.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["htwk-leipzig.de"], "name": "Hochschule f\u00fcr Technik, Wirtschaft und Kultur Leipzig (FH)"}, {"web_pages": ["http://www.htwm.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["htwm.de"], "name": "Hochschule Mittweida (FH)"}, {"web_pages": ["http://www.htw-saarland.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["htw-saarland.de"], "name": "Hochschule f\u00fcr Technik und Wirtschaft des Saarlandes"}, {"web_pages": ["http://www.hu-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hu-berlin.de"], "name": "Humboldt Universit\u00e4t Berlin"}, {"web_pages": ["http://www.hwp-hamburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["hwp-hamburg.de"], "name": "HWP - Hamburger Universit\u00e4t f\u00fcr Wirtschaft und Politik"}, {"web_pages": ["http://www.ihi-zittau.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ihi-zittau.de"], "name": "Internationales Hochschulinstitut Zittau"}, {"web_pages": ["http://www.international.fh-aalen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["international.fh-aalen.de"], "name": "Internationale Fachhochschule Aalen"}, {"web_pages": ["http://www.ism-dortmund.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ism-dortmund.de"], "name": "International School of Management ISM Dortmund"}, {"web_pages": ["http://www.isnm.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["isnm.de"], "name": "International School of New Media, University of L\u00fcbeck"}, {"web_pages": ["http://www.i-u.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["i-u.de"], "name": "International University in Germany"}, {"web_pages": ["http://www.jacobs-university.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["jacobs-university.de"], "name": "Jacobs University Bremen"}, {"web_pages": ["http://www.karlshochschule.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["karlshochschule.de"], "name": "Karlshochschule International University"}, {"web_pages": ["http://www.kath-fh-nord.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kath-fh-nord.de"], "name": "Katholische Fachhochschule Norddeutschland"}, {"web_pages": ["http://www.kfb-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kfb-berlin.de"], "name": "Katholische Fachhochschule Berlin (KFB)"}, {"web_pages": ["http://www.kfh-Freiburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kfh-Freiburg.de"], "name": "Katholische Fachhochschule Freiburg, Hochschule f\u00fcr Sozialwesen, Religionsp\u00e4dagogik und Pflege"}, {"web_pages": ["http://www.kfh-mainz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kfh-mainz.de"], "name": "Katholische Fachhochschule Mainz"}, {"web_pages": ["http://www.kfhnw.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kfhnw.de"], "name": "Katholische Fachhochschule Nordrhein-Westfalen"}, {"web_pages": ["http://www.kh-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kh-berlin.de"], "name": "Kunsthochschule Berlin-Weissensee, Hochschule f\u00fcr Gestaltung"}, {"web_pages": ["http://www.khsa.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["khsa.de"], "name": "Katholische Hochschule f\u00fcr Soziale Arbeit Saarbr\u00fccken"}, {"web_pages": ["http://www.ksfh.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ksfh.de"], "name": "Katholische Stiftungsfachhochschule M\u00fcnchen"}, {"web_pages": ["http://www.ku-eichstaett.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ku-eichstaett.de"], "name": "Katholische Universit\u00e4t Eichst\u00e4tt"}, {"web_pages": ["http://www.kunstakademie-duesseldorf.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kunstakademie-duesseldorf.de"], "name": "Kunstakademie D\u00fcsseldorf."}, {"web_pages": ["http://www.merkur-fh.org/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["merkur-fh.org"], "name": "Merkur Internationale FH Karlsruhe"}, {"web_pages": ["http://www.merz-akademie.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["merz-akademie.de"], "name": "Merz Akademie, Hochschule f\u00fcr Gestaltung Stuttgart"}, {"web_pages": ["http://www.mfh-iserlohn.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["mfh-iserlohn.de"], "name": "M\u00e4rkische Fachhochschule Iserlohn"}, {"web_pages": ["http://www.mh-hannover.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["mh-hannover.de"], "name": "Medizinische Hochschule Hannover"}, {"web_pages": ["http://www.mh-trossingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["mh-trossingen.de"], "name": "Staatliche Hochschule f\u00fcr Musik"}, {"web_pages": ["http://www.mu-luebeck.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["mu-luebeck.de"], "name": "Medizinische Universit\u00e4t L\u00fcbeck"}, {"web_pages": ["http://www.muthesius.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["muthesius.de"], "name": "Muthesius-Hochschule, Fachhochschule f\u00fcr Kunst und Gestaltung"}, {"web_pages": ["http://www.nordakademie.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["nordakademie.de"], "name": "Nordakademie, Staatlich anerkannte private Fachhochschule mit dualen Studieng\u00e4ngen"}, {"web_pages": ["http://www.paderborn.de/theofak/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["paderborn.de"], "name": "Theologische Fakult\u00e4t Paderborn"}, {"web_pages": ["http://www.pfh-goettingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["pfh-goettingen.de"], "name": "Private Fachhochschule G\u00f6ttingen"}, {"web_pages": ["http://www.ph-erfurt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ph-erfurt.de"], "name": "P\u00e4dagogische Hochschule Erfurt/M\u00fchlhausen"}, {"web_pages": ["http://www.ph-freiburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ph-freiburg.de"], "name": "P\u00e4dagogische Hochschule Freiburg"}, {"web_pages": ["http://www.ph-gmuend.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ph-gmuend.de"], "name": "P\u00e4dagogische Hochschule Schw\u00e4bisch Gm\u00fcnd"}, {"web_pages": ["http://www.ph-heidelberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ph-heidelberg.de"], "name": "P\u00e4dagogische Hochschule Heidelberg"}, {"web_pages": ["http://www.philtheol-augustin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["philtheol-augustin.de"], "name": "Philosophisch-Theologische Hochschule SVD Sankt Augustin"}, {"web_pages": ["http://www.ph-karlsruhe.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ph-karlsruhe.de"], "name": "P\u00e4dagogische Hochschule Karlsruhe"}, {"web_pages": ["http://www.ph-ludwigsburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ph-ludwigsburg.de"], "name": "P\u00e4dagogische Hochschule Ludwigsburg"}, {"web_pages": ["http://www.ph-weingarten.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ph-weingarten.de"], "name": "P\u00e4dagogische Hochschule Weingarten"}, {"web_pages": ["http://www.popakademie.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["popakademie.de"], "name": "Popakademie Baden-W\u00fcrttemberg"}, {"web_pages": ["http://www.privatfh-da.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["privatfh-da.de"], "name": "Private FernFachhochschule Darmstadt"}, {"web_pages": ["http://www.pth-bb.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["pth-bb.de"], "name": "Philosophisch-Theologische Hochschule der Salesianer Don Boscos"}, {"web_pages": ["http://www.pth-muenster.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["pth-muenster.de"], "name": "Philosophisch-Theologische Hochschule M\u00fcnster"}, {"web_pages": ["http://www.pthv.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["pthv.de"], "name": "Philosophisch-Theologische Hochschule Vallendar der Gesellschaft des Katholischen Apostolates (Pallottiner)"}, {"web_pages": ["http://www.rauheshaus.de/fachhochschule/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["rauheshaus.de"], "name": "Evangelische Fachhochschule f\u00fcr Sozialp\u00e4dagogik der \"Diakonenanstalt des Rauhen Hauses\" Hamburg"}, {"web_pages": ["http://www.rfh-koeln.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["rfh-koeln.de"], "name": "Rheinische Fachhochschule K\u00f6ln"}, {"web_pages": ["http://www.ruhr-uni-bochum.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["ruhr-uni-bochum.de"], "name": "Ruhr-Universit\u00e4t Bochum"}, {"web_pages": ["http://www.rwth-aachen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["rwth-aachen.de"], "name": "Rheinisch Westf\u00e4lische Technische Hochschule Aachen"}, {"web_pages": ["http://www.selk.de/LThH/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["selk.de"], "name": "Lutherische Theologische Hochschule Oberursel"}, {"web_pages": ["http://www.siewerth-akademie.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["siewerth-akademie.de"], "name": "Gustav-Siewerth-Akademie"}, {"web_pages": ["http://www.siu-heidelberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["siu-heidelberg.de"], "name": "Schiller International University, Heidelberg"}, {"web_pages": ["http://www.srh-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["srh-berlin.de"], "name": "SRH University of Applied Sciences"}, {"web_pages": ["http://www.st-georgen.uni-frankfurt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["st-georgen.uni-frankfurt.de"], "name": "Philosophisch-Theologische Hochschule Sankt Georgen"}, {"web_pages": ["http://www.stw.de/shb/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["stw.de"], "name": "Steinbeis-Hochschule-Berlin"}, {"web_pages": ["http://www.tfh-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tfh-berlin.de"], "name": "Technische Fachhochschule Berlin"}, {"web_pages": ["http://www.tfh-bochum.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tfh-bochum.de"], "name": "Technische Fachhochschule Georg Agricola f\u00fcr Rohstoff, Energie und, Umwelt zu Bochum"}, {"web_pages": ["http://www.tfh-wildau.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tfh-wildau.de"], "name": "Technische Fachhochschule Wildau"}, {"web_pages": ["http://www.thh-friedensau.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["thh-friedensau.de"], "name": "Theologische Hochschule Friedensau"}, {"web_pages": ["http://www.tiho-hannover.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tiho-hannover.de"], "name": "Tier\u00e4rztliche Hochschule Hannover"}, {"web_pages": ["http://www.tu-berlin.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-berlin.de"], "name": "Technische Universit\u00e4t Berlin"}, {"web_pages": ["http://www.tu-bs.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-bs.de"], "name": "Technische Universit\u00e4t Carolo-Wilhelmina Braunschweig"}, {"web_pages": ["http://www.tu-chemnitz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-chemnitz.de"], "name": "Technische Universit\u00e4t Chemnitz"}, {"web_pages": ["http://www.tu-clausthal.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-clausthal.de"], "name": "Technische Universit\u00e4t Clausthal"}, {"web_pages": ["http://www.tu-cottbus.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-cottbus.de"], "name": "Brandenburgische Technische Universit\u00e4t Cottbus"}, {"web_pages": ["https://www.tu-darmstadt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-darmstadt.de"], "name": "Technische Universit\u00e4t Darmstadt"}, {"web_pages": ["http://www.tu-dresden.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-dresden.de"], "name": "Technische Universit\u00e4t Dresden"}, {"web_pages": ["http://www.tu-freiberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-freiberg.de"], "name": "Technische Universit\u00e4t Bergakademie Freiberg"}, {"web_pages": ["http://www.tu-harburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-harburg.de"], "name": "Technische Universit\u00e4t Hamburg-Harburg"}, {"web_pages": ["http://www.tu-ilmenau.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tu-ilmenau.de"], "name": "Technische Universit\u00e4t Ilmenau"}, {"web_pages": ["http://www.tum.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["tum.de", "tum.edu"], "name": "Technische Universit\u00e4t M\u00fcnchen"}, {"web_pages": ["http://www.uni-augsburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-augsburg.de"], "name": "Universit\u00e4t Augsburg"}, {"web_pages": ["http://www.uni-bamberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-bamberg.de"], "name": "Otto-Friedrich Universit\u00e4t Bamberg"}, {"web_pages": ["http://www.uni-bayreuth.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-bayreuth.de"], "name": "Universit\u00e4t Bayreuth"}, {"web_pages": ["http://www.uni-bielefeld.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-bielefeld.de"], "name": "Universit\u00e4t Bielefeld"}, {"web_pages": ["http://www.uni-bonn.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-bonn.de"], "name": "Rheinische Friedrich-Wilhelms Universit\u00e4t Bonn"}, {"web_pages": ["http://www.uni-bremen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-bremen.de"], "name": "Universit\u00e4t Bremen"}, {"web_pages": ["http://www.unibw-hamburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["unibw-hamburg.de"], "name": "Universit\u00e4t der Bundeswehr Hamburg"}, {"web_pages": ["http://www.unibw-muenchen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["unibw-muenchen.de"], "name": "Universit\u00e4t der Bundeswehr M\u00fcnchen"}, {"web_pages": ["http://www.uni-dortmund.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-dortmund.de"], "name": "Universit\u00e4t Dortmund"}, {"web_pages": ["http://www.uni-duesseldorf.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-duesseldorf.de"], "name": "Heinrich-Heine Universit\u00e4t D\u00fcsseldorf"}, {"web_pages": ["http://www.uni-duisburg-essen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-duisburg-essen.de"], "name": "Universit\u00e4t Duisburg-Essen"}, {"web_pages": ["http://www.uni-erfurt.de/phil-theol/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-erfurt.de"], "name": "Philosophisch-Theologisches Studium Erfurt, Staatlich anerkannte Wissenschaftliche Hochschule"}, {"web_pages": ["http://www.uni-erfurt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-erfurt.de"], "name": "Universit\u00e4t Erfurt"}, {"web_pages": ["http://www.uni-erlangen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-erlangen.de"], "name": "Friedrich-Alexander Universit\u00e4t Erlangen-N\u00fcrnberg"}, {"web_pages": ["http://www.uni-flensburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-flensburg.de"], "name": "Universit\u00e4t Flensburg"}, {"web_pages": ["http://www.uni-frankfurt.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-frankfurt.de"], "name": "Johann Wolfgang Goethe Universit\u00e4t Frankfurt am Main"}, {"web_pages": ["http://www.uni-freiburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-freiburg.de"], "name": "Albert-Ludwigs-Universit\u00e4t Freiburg"}, {"web_pages": ["http://www.uni-giessen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-giessen.de"], "name": "Justus Liebig Universit\u00e4t Gie\u00dfen"}, {"web_pages": ["http://www.uni-goettingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-goettingen.de"], "name": "Georg-August Universit\u00e4t G\u00f6ttingen"}, {"web_pages": ["http://www.uni-greifswald.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-greifswald.de"], "name": "Ernst-Moritz-Arndt Universit\u00e4t Greifswald"}, {"web_pages": ["http://www.uni-halle.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-halle.de"], "name": "Martin-Luther Universit\u00e4t Halle-Wittenberg"}, {"web_pages": ["http://www.uni-hamburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-hamburg.de"], "name": "Universit\u00e4t Hamburg"}, {"web_pages": ["http://www.uni-hannover.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-hannover.de"], "name": "Universit\u00e4t Hannover"}, {"web_pages": ["http://www.uni-heidelberg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-heidelberg.de"], "name": "Ruprecht-Karls-Universit\u00e4t Heidelberg"}, {"web_pages": ["http://www.uni-hildesheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-hildesheim.de"], "name": "Universit\u00e4t Hildesheim"}, {"web_pages": ["http://www.uni-hohenheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-hohenheim.de"], "name": "Universit\u00e4t Hohenheim"}, {"web_pages": ["http://www.uni-jena.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-jena.de"], "name": "Friedrich-Schiller Universit\u00e4t Jena"}, {"web_pages": ["http://www.kit.edu/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["kit.edu"], "name": "Karlsruher Institut f\u00fcr Technologie"}, {"web_pages": ["http://www.uni-kassel.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-kassel.de"], "name": "Universit\u00e4t Kassel"}, {"web_pages": ["http://www.uni-kiel.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-kiel.de"], "name": "Christian-Albrechts-Universit\u00e4t Kiel"}, {"web_pages": ["http://www.uni-kl.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-kl.de"], "name": "Universit\u00e4t Kaiserslautern"}, {"web_pages": ["http://www.uni-koblenz-landau.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-koblenz-landau.de"], "name": "Universit\u00e4t Koblenz-Landau"}, {"web_pages": ["http://www.uni-koeln.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-koeln.de"], "name": "Universit\u00e4t K\u00f6ln"}, {"web_pages": ["http://www.uni-konstanz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-konstanz.de"], "name": "Universit\u00e4t Konstanz"}, {"web_pages": ["http://www.uni-leipzig.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-leipzig.de"], "name": "Universit\u00e4t Leipzig"}, {"web_pages": ["http://www.uni-lueneburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-lueneburg.de"], "name": "Universit\u00e4t L\u00fcneburg"}, {"web_pages": ["http://www.uni-magdeburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-magdeburg.de"], "name": "Otto-von-Guericke Universit\u00e4t Magdeburg"}, {"web_pages": ["http://www.uni-mainz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-mainz.de"], "name": "Johannes-Gutenberg Universit\u00e4t Mainz"}, {"web_pages": ["http://www.uni-mannheim.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-mannheim.de"], "name": "Universit\u00e4t Mannheim"}, {"web_pages": ["http://www.uni-marburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-marburg.de"], "name": "Phillips-Universit\u00e4t Marburg"}, {"web_pages": ["http://www.uni-muenchen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-muenchen.de"], "name": "Ludwig-Maximilians-Universit\u00e4t M\u00fcnchen"}, {"web_pages": ["http://www.lmu.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["lmu.de"], "name": "Ludwig-Maximilians-Universit\u00e4t M\u00fcnchen"}, {"web_pages": ["http://www.uni-muenster.de/", "http://www.wwu.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-muenster.de", "wwu.de"], "name": "Westf\u00e4lische Wilhelms-Universit\u00e4t M\u00fcnster"}, {"web_pages": ["http://www.uni-oldenburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-oldenburg.de"], "name": "Carl von Ossietzky Universit\u00e4t Oldenburg"}, {"web_pages": ["http://www.uni-osnabrueck.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-osnabrueck.de"], "name": "Universit\u00e4t Osnabr\u00fcck"}, {"web_pages": ["http://www.uni-paderborn.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-paderborn.de"], "name": "Universit\u00e4t Paderborn"}, {"web_pages": ["http://www.uni-passau.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-passau.de"], "name": "Universit\u00e4t Passau"}, {"web_pages": ["http://www.uni-potsdam.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-potsdam.de"], "name": "Universit\u00e4t Potsdam"}, {"web_pages": ["http://www.uni-polsdam.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-polsdam.de"], "name": "Universit\u00e4t Polsdam"}, {"web_pages": ["http://www.uni-regensburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-regensburg.de"], "name": "Universit\u00e4t Regensburg"}, {"web_pages": ["http://www.uni-rostock.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-rostock.de"], "name": "Universit\u00e4t Rostock"}, {"web_pages": ["http://www.uni-saarland.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-saarland.de"], "name": "Universit\u00e4t des Saarlandes"}, {"web_pages": ["http://www.uni-siegen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-siegen.de"], "name": "Universit\u00e4t Siegen"}, {"web_pages": ["http://www.uni-stuttgart.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-stuttgart.de"], "name": "Universit\u00e4t Stuttgart"}, {"web_pages": ["http://www.uni-trier.de/uni/theo/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-trier.de"], "name": "Theologische Fakult\u00e4t Trier"}, {"web_pages": ["http://www.uni-trier.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-trier.de"], "name": "Universit\u00e4t Trier"}, {"web_pages": ["http://www.uni-tuebingen.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-tuebingen.de"], "name": "Eberhard-Karls-Universit\u00e4t T\u00fcbingen"}, {"web_pages": ["http://www.uni-ulm.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-ulm.de"], "name": "Universit\u00e4t Ulm"}, {"web_pages": ["http://www.uni-vechta.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-vechta.de"], "name": "Hochschule Vechta"}, {"web_pages": ["http://www.uni-weimar.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-weimar.de"], "name": "Bauhaus Universit\u00e4t Weimar"}, {"web_pages": ["http://www.uni-wh.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-wh.de"], "name": "Private Universit\u00e4t Witten/Herdecke"}, {"web_pages": ["http://www.uni-wuerzburg.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-wuerzburg.de"], "name": "Bayerische Julius-Maximilians-Universit\u00e4t W\u00fcrzburg"}, {"web_pages": ["http://www.uni-wuppertal.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-wuppertal.de"], "name": "Bergische Universit\u00e4t Gesamthochschule Wuppertal"}, {"web_pages": ["http://www.uni-wuppertal.de/inst/kiho/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["uni-wuppertal.de"], "name": "Kirchliche Hochschule Wuppertal"}, {"web_pages": ["http://www.whu-koblenz.de/"], "alpha_two_code": "DE",  "country": "Germany", "domains": ["whu-koblenz.de"], "name": "Wissenschaftliche Hochschule f\u00fcr Unternehmensf\u00fchrung, Otto-Beisheim Hochschule"}, {"web_pages": ["http://www.dhbw-mannheim.de/"], "alpha_two_code": "DE", "state-province": "null", "country": "Germany", "domains": ["dhbw-mannheim.de"], "name": "Duale Hochschule Baden-Wuerttemberg Mannheim"}]
```

first Command:
```javascript
db.createCollection("uniInfo")
```
result:
```
{ "ok" : 1 }
```
second Command:
```javascript
db.uniInfo.insert(
    [
    {
        "web_pages": [
            "http://www.afeka.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "afeka.ac.il"
        ],
        "name": "Afeka Tel Aviv Academic College of Engineering"
    },
    {
        "web_pages": [
            "http://www.ariel.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "ariel.ac.il"
        ],
        "name": "Ariel University Center of Samaria"
    },
    {
        "web_pages": [
            "http://www.ash-college.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "ash-college.ac.il"
        ],
        "name": "Ashkelon Academic College"
    },
    {
        "web_pages": [
            "http://www.bezalel.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "bezalel.ac.il"
        ],
        "name": "Bezalel Academy of Art and Design"
    },
    {
        "web_pages": [
            "http://www.bgu.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "bgu.ac.il"
        ],
        "name": "Ben-Gurion University of the Negev"
    },
    {
        "web_pages": [
            "http://www.biu.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "biu.ac.il"
        ],
        "name": "Bar-Ilan University"
    },
    {
        "web_pages": [
            "http://www.clb.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "clb.ac.il"
        ],
        "name": "Acdemic Center for Law and Business"
    },
    {
        "web_pages": [
            "http://www.colman.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "colman.ac.il"
        ],
        "name": "College of Management"
    },
    {
        "web_pages": [
            "http://www.galilcol.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "galilcol.ac.il"
        ],
        "name": "Galillee College"
    },
    {
        "web_pages": [
            "http://www.haifa.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "haifa.ac.il"
        ],
        "name": "University of Haifa"
    },
    {
        "web_pages": [
            "http://www.huji.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "huji.ac.il"
        ],
        "name": "Hebrew University of Jerusalem"
    },
    {
        "web_pages": [
            "http://www.idc.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "idc.ac.il"
        ],
        "name": "The Interdisciplinary Center Herzliya"
    },
    {
        "web_pages": [
            "http://www.juc.edu/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "juc.edu"
        ],
        "name": "Jerusalem University College"
    },
    {
        "web_pages": [
            "http://www.openu.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "openu.ac.il"
        ],
        "name": "Open University of Israel"
    },
    {
        "web_pages": [
            "http://rbni.technion.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "rbni.technion.ac.il"
        ],
        "name": "Russell Berrie Nanotechnology Institute"
    },
    {
        "web_pages": [
            "http://www.sce.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "sce.ac.il"
        ],
        "name": "Sami Shamoon College of Engineering"
    },
    {
        "web_pages": [
            "http://www.shenkar.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "shenkar.ac.il"
        ],
        "name": "Shenkar School of Engineering & Design"
    },
    {
        "web_pages": [
            "http://www.tau.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "tau.ac.il"
        ],
        "name": "Tel Aviv University"
    },
    {
        "web_pages": [
            "http://www.technion.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "technion.ac.il"
        ],
        "name": "Technion - Israel Institute of Technology"
    },
    {
        "web_pages": [
            "http://www.weizmann.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "weizmann.ac.il"
        ],
        "name": "Weizmann Institute of Science"
    },
    {
        "web_pages": [
            "http://www.wgalil.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "wgalil.ac.il"
        ],
        "name": "Western Galilee College"
    },
    {
        "web_pages": [
            "http://www.yvc.ac.il/"
        ],
        "alpha_two_code": "IL",
        "country": "Israel",
        "domains": [
            "yvc.ac.il"
        ],
        "name": "Emeq Yizrael College"
    },
    {
        "web_pages": [
            "http://www.akad.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "akad.de"
        ],
        "name": "AKAD Hochschulen f\u00fcr Berufst\u00e4tige, Fachhochschule Leipzig"
    },
    {
        "web_pages": [
            "http://www.akad.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "akad.de"
        ],
        "name": "Hochschule f\u00fcr Berufst\u00e4tige Rendsburg"
    },
    {
        "web_pages": [
            "http://www.asfh-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "asfh-berlin.de"
        ],
        "name": "Alice-Salomon-Fachhochschule f\u00fcr Sozialarbeit und Sozialp\u00e4dagogik Berlin"
    },
    {
        "web_pages": [
            "http://www.augustana.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "augustana.de"
        ],
        "name": "Augustana Hochschule Neuendettelsau"
    },
    {
        "web_pages": [
            "http://www.bethel.de/kiho/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "bethel.de"
        ],
        "name": "Kirchliche Hochschule Bethel"
    },
    {
        "web_pages": [
            "http://www.bits-iserlohn.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "bits-iserlohn.de"
        ],
        "name": "BiTS - Business and Information Technology School gGmbH"
    },
    {
        "web_pages": [
            "http://www.cbs.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "cbs.de"
        ],
        "name": "Cologne Business School"
    },
    {
        "web_pages": [
            "http://www.dhbw.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "dhbw.de"
        ],
        "name": "Duale Hochschule Baden-W\u00fcrttemberg"
    },
    {
        "web_pages": [
            "http://www.dhv-speyer.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "dhv-speyer.de"
        ],
        "name": "Deutsche Hochschule f\u00fcr Verwaltungswissenschaften Speyer"
    },
    {
        "web_pages": [
            "http://www.diploma.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "diploma.de"
        ],
        "name": "DIPLOMA-Fachhochschule \u00d6lsnitz/Vogtland"
    },
    {
        "web_pages": [
            "http://www.diploma.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "diploma.de"
        ],
        "name": "Fachhochschule Nordhessen"
    },
    {
        "web_pages": [
            "http://www.dshs-koeln.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "dshs-koeln.de"
        ],
        "name": "Deutsche Sporthochschule K\u00f6ln"
    },
    {
        "web_pages": [
            "http://www.eap.net/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "eap.net"
        ],
        "name": "E.A.P. Europ\u00e4ische Wirtschaftshochschule Berlin"
    },
    {
        "web_pages": [
            "http://www.eba-muenchen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "eba-muenchen.de"
        ],
        "name": "Europ\u00e4ische Betriebswirtschafts-Akademie"
    },
    {
        "web_pages": [
            "http://www.ebs.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ebs.de"
        ],
        "name": "European Business School Schlo\u00df Reichartshausen"
    },
    {
        "web_pages": [
            "http://www.ecla.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ecla.de"
        ],
        "name": "European College of Liberal Arts"
    },
    {
        "web_pages": [
            "http://www.efh-bochum.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "efh-bochum.de"
        ],
        "name": "Evangelische Fachhochschule Rheinland-Westfalen-Lippe"
    },
    {
        "web_pages": [
            "https://www.eh-darmstadt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "eh-darmstadt.de"
        ],
        "name": "Evangelische Fachhochschule Darmstadt"
    },
    {
        "web_pages": [
            "http://www.efh-freiburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "efh-freiburg.de"
        ],
        "name": "Evangelische Fachhochschule Freiburg, Hochschule f\u00fcr Soziale Arbeit, Diakonie und Religionsp\u00e4dagogik"
    },
    {
        "web_pages": [
            "http://www.efh-hannover.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "efh-hannover.de"
        ],
        "name": "Evangelische Fachhochschule Hannover"
    },
    {
        "web_pages": [
            "http://www.efhlu.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "efhlu.de"
        ],
        "name": "Evangelische Fachhochschule Ludwigshafen Hochschule f\u00fcr Sozial- und Gesundheitswesen"
    },
    {
        "web_pages": [
            "http://www.efh-reutlingen-ludwigsburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "efh-reutlingen-ludwigsburg.de"
        ],
        "name": "Evangelische Fachhochschule Reutlingen-Ludwigsburg, Hochschule f\u00fcr Soziale Arbeit, Religionsp\u00e4dagogik und Diakonie"
    },
    {
        "web_pages": [
            "http://www.ehs-dresden.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ehs-dresden.de"
        ],
        "name": "Evangelische Hochschule f\u00fcr Soziale Arbeit Dresden (FH)"
    },
    {
        "web_pages": [
            "http://www.ems-mainz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ems-mainz.de"
        ],
        "name": "European Management School"
    },
    {
        "web_pages": [
            "http://www.eufh.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "eufh.de"
        ],
        "name": "Europ\u00e4ische Fachhochschule"
    },
    {
        "web_pages": [
            "http://www.euv-frankfurt-o.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "euv-frankfurt-o.de"
        ],
        "name": "Europa-Universit\u00e4t Viadrina Frankfurt (Oder)"
    },
    {
        "web_pages": [
            "http://www.evfh-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "evfh-berlin.de"
        ],
        "name": "Evangelische Fachhochschule Berlin, Fachhochschule f\u00fcr Sozialarbeit und Sozialp\u00e4dagogik"
    },
    {
        "web_pages": [
            "http://www.evfh-nuernberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "evfh-nuernberg.de"
        ],
        "name": "Evangelische Fachhochschule N\u00fcrnberg"
    },
    {
        "web_pages": [
            "http://www.fern-fh.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fern-fh.de"
        ],
        "name": "Fern-Fachhochschule Hamburg"
    },
    {
        "web_pages": [
            "http://www.fernuni-hagen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fernuni-hagen.de"
        ],
        "name": "Fernuniversit\u00e4t Gesamthochschule Hagen"
    },
    {
        "web_pages": [
            "http://www.fh-aachen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-aachen.de"
        ],
        "name": "Fachhochschule Aachen"
    },
    {
        "web_pages": [
            "http://www.fh-aschaffenburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-aschaffenburg.de"
        ],
        "name": "Fachhochschule Aschaffenburg"
    },
    {
        "web_pages": [
            "http://www.fh-augsburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-augsburg.de"
        ],
        "name": "Fachhochschule Augsburg"
    },
    {
        "web_pages": [
            "http://www.fh-bad-honnef.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-bad-honnef.de"
        ],
        "name": "Internationale Fachhochschule Bad Honnef"
    },
    {
        "web_pages": [
            "http://www.fh-biberach.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-biberach.de"
        ],
        "name": "Fachhochschule Biberach, Hochschule f\u00fcr Bauwesen und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-bielefeld.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-bielefeld.de"
        ],
        "name": "Fachhochschule Bielefeld"
    },
    {
        "web_pages": [
            "http://www.fh-bingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-bingen.de"
        ],
        "name": "Fachhochschule Bingen"
    },
    {
        "web_pages": [
            "http://www.fh-bochum.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-bochum.de"
        ],
        "name": "Fachhochschule Bochum"
    },
    {
        "web_pages": [
            "http://www.hochschule-bonn-rhein-sieg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hochschule-bonn-rhein-sieg.de",
            "h-brs.de"
        ],
        "name": "Hochschule Bonn-Rhein-Sieg"
    },
    {
        "web_pages": [
            "http://www.fh-brandenburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-brandenburg.de"
        ],
        "name": "Fachhochschule Brandenburg"
    },
    {
        "web_pages": [
            "http://www.th-brandenburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "th-brandenburg.de"
        ],
        "name": "Technische Hochschule Brandenburg"
    },
    {
        "web_pages": [
            "http://www.th-deg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "th-deg.de"
        ],
        "name": "Technische Hochschule Deggendorf"
    },
    {
        "web_pages": [
            "http://www.fh-dortmund.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-dortmund.de"
        ],
        "name": "Fachhochschule Dortmund"
    },
    {
        "web_pages": [
            "http://www.hs-duesseldorf.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-duesseldorf.de"
        ],
        "name": "Hochschule D\u00fcsseldorf"
    },
    {
        "web_pages": [
            "http://www.fhdw.bib.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhdw.bib.de"
        ],
        "name": "Fachhochschule f\u00fcr die Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fhdw.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhdw.de"
        ],
        "name": "Fachhochschule der Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-eberswalde.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-eberswalde.de"
        ],
        "name": "Fachhochschule Eberswalde"
    },
    {
        "web_pages": [
            "http://www.fh-erfurt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-erfurt.de"
        ],
        "name": "Fachhochschule Erfurt"
    },
    {
        "web_pages": [
            "http://www.fh-flensburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-flensburg.de"
        ],
        "name": "Fachhochschule Flensburg"
    },
    {
        "web_pages": [
            "http://www.fh-frankfurt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-frankfurt.de"
        ],
        "name": "Fachhochschule Frankfurt am Main"
    },
    {
        "web_pages": [
            "http://www.fh-fresenius.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-fresenius.de"
        ],
        "name": "Europa Fachhochschule Fresenius"
    },
    {
        "web_pages": [
            "http://www.fh-furtwangen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-furtwangen.de"
        ],
        "name": "Fachhochschule Furtwangen, Hochschule f\u00fcr Technik und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-gelsenkirchen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-gelsenkirchen.de"
        ],
        "name": "Fachhochschule Gelsenkirchen"
    },
    {
        "web_pages": [
            "http://www.fh-giessen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-giessen.de"
        ],
        "name": "Fachhochschule Gie\u00dfen-Friedberg"
    },
    {
        "web_pages": [
            "http://www.fh-hamburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-hamburg.de"
        ],
        "name": "Fachhochschule Hamburg"
    },
    {
        "web_pages": [
            "http://www.fh-hannover.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-hannover.de"
        ],
        "name": "Fachhochschule Hannover"
    },
    {
        "web_pages": [
            "http://www.fh-heidelberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-heidelberg.de"
        ],
        "name": "Fachhochschule Heidelberg"
    },
    {
        "web_pages": [
            "http://www.fh-heilbronn.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-heilbronn.de"
        ],
        "name": "Fachhochschule Heilbronn, Hochschule f\u00fcr Technik und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-hildesheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-hildesheim.de"
        ],
        "name": "Fachhochschule Hildesheim/Holzminden/G\u00f6ttingen, Hochschule f\u00fcr angewandte Wissenschaft und Kunst"
    },
    {
        "web_pages": [
            "http://www.fh-hof.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-hof.de"
        ],
        "name": "Fachhochschule Hof"
    },
    {
        "web_pages": [
            "http://www.fh-ingolstadt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-ingolstadt.de"
        ],
        "name": "Fachhochschule Ingolstadt"
    },
    {
        "web_pages": [
            "http://www.fh-isny.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-isny.de"
        ],
        "name": "Fachhochschule und Berufskollegs NTA, Prof.Dr. Gr\u00fcbler gemein. GmbH"
    },
    {
        "web_pages": [
            "http://www.fh-jena.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-jena.de"
        ],
        "name": "Fachhochschule Jena"
    },
    {
        "web_pages": [
            "http://www.fh-karlsruhe.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-karlsruhe.de"
        ],
        "name": "Fachhochschule Karlsruhe, Hochschule f\u00fcr Technik"
    },
    {
        "web_pages": [
            "http://www.fh-Kempten.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-Kempten.de"
        ],
        "name": "Fachhochschule Kempten, Hochschule f\u00fcr Technik und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-kiel.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-kiel.de"
        ],
        "name": "Fachhochschule Kiel"
    },
    {
        "web_pages": [
            "http://www.fh-kl.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-kl.de"
        ],
        "name": "Fachhochschule Kaiserslautern"
    },
    {
        "web_pages": [
            "http://www.fh-koblenz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-koblenz.de"
        ],
        "name": "Fachhochschule Koblenz"
    },
    {
        "web_pages": [
            "http://www.fh-koeln.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-koeln.de"
        ],
        "name": "Fachhochschule K\u00f6ln"
    },
    {
        "web_pages": [
            "http://www.fh-konstanz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-konstanz.de"
        ],
        "name": "Fachhochschule Konstanz, Hochschule f\u00fcr Technik, Wirtschaft und Gestaltung"
    },
    {
        "web_pages": [
            "http://www.fhkt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhkt.de"
        ],
        "name": "Staatlich anerkannte Fachhochschule f\u00fcr Kunsttherapie"
    },
    {
        "web_pages": [
            "http://www.fh-landshut.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-landshut.de"
        ],
        "name": "Fachhochschule Landshut, Hochschule f\u00fcr Wirtschaft - Sozialwesen - Technik"
    },
    {
        "web_pages": [
            "http://www.fh-lausitz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-lausitz.de"
        ],
        "name": "Fachhochschule Lausitz"
    },
    {
        "web_pages": [
            "http://www.fh-lippe.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-lippe.de"
        ],
        "name": "Fachhochschule Lippe"
    },
    {
        "web_pages": [
            "http://www.fh-ludwigshafen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-ludwigshafen.de"
        ],
        "name": "Fachhochschule Ludwigshafen, Hochschule f\u00fcr Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-luebeck.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-luebeck.de"
        ],
        "name": "Fachhochschule L\u00fcbeck"
    },
    {
        "web_pages": [
            "http://www.fh-mainz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-mainz.de"
        ],
        "name": "Fachhochschule Mainz"
    },
    {
        "web_pages": [
            "http://www.fh-mannheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-mannheim.de"
        ],
        "name": "Fachhochschule Mannheim, Hochschule f\u00fcr Technik und Gestaltung"
    },
    {
        "web_pages": [
            "http://www.fh-merseburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-merseburg.de"
        ],
        "name": "Fachhochschule Merseburg"
    },
    {
        "web_pages": [
            "http://www.fhm-mittelstand.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhm-mittelstand.de"
        ],
        "name": "Fachhochschule des Mittelstandes (FHM)"
    },
    {
        "web_pages": [
            "http://www.fh-muenchen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-muenchen.de"
        ],
        "name": "Fachhochschule M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.hm.edu/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hm.edu"
        ],
        "name": "Hochschule M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.fh-muenster.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-muenster.de"
        ],
        "name": "Fachhochschule M\u00fcnster"
    },
    {
        "web_pages": [
            "http://www.fh-nb.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-nb.de"
        ],
        "name": "Fachhochschule Neubrandenburg"
    },
    {
        "web_pages": [
            "http://www.hs-neu-ulm.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-neu-ulm.de"
        ],
        "name": "Hochschule Neu-Ulm, Hochschule Neu-Ulm University of applied sciences"
    },
    {
        "web_pages": [
            "http://www.fh-niederrhein.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-niederrhein.de"
        ],
        "name": "Fachhochschule Niederrhein"
    },
    {
        "web_pages": [
            "http://www.fhnon.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhnon.de"
        ],
        "name": "Fachhochschule Nordostniedersachsen"
    },
    {
        "web_pages": [
            "http://www.fh-nordhausen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-nordhausen.de"
        ],
        "name": "Fachhochschule Nordhausen"
    },
    {
        "web_pages": [
            "http://www.fh-nuernberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-nuernberg.de"
        ],
        "name": "Georg-Simon-Ohm-Fachhochschule N\u00fcrnberg"
    },
    {
        "web_pages": [
            "http://www.fh-nuertingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-nuertingen.de"
        ],
        "name": "Fachhochschule N\u00fcrtingen, Hochschule f\u00fcr Wirtschaft, Landwirtschaft und Landespflege"
    },
    {
        "web_pages": [
            "http://www.fhoebb.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhoebb.de"
        ],
        "name": "Fachhochschule f\u00fcr das \u00f6ffentliche Bibliothekswesen Bonn"
    },
    {
        "web_pages": [
            "http://www.fh-offenburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-offenburg.de"
        ],
        "name": "Fachhochschule Offenburg, Hochschule f\u00fcr Technik und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-oow.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-oow.de"
        ],
        "name": "Fachhochschule Oldenburg/Ostfriesland/Wilhelmshaven"
    },
    {
        "web_pages": [
            "http://www.fh-osnabrueck.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-osnabrueck.de"
        ],
        "name": "Fachhochschule Osnabr\u00fcck"
    },
    {
        "web_pages": [
            "http://www.fh-ottersberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-ottersberg.de"
        ],
        "name": "Freie Kunst-Studienst\u00e4tte Ottersberg"
    },
    {
        "web_pages": [
            "http://www.fh-pforzheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-pforzheim.de"
        ],
        "name": "Fachhochschule Pforzheim, Hochschule f\u00fcr Gestaltung, Technik und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-potsdam.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-potsdam.de"
        ],
        "name": "Fachhochschule Potsdam"
    },
    {
        "web_pages": [
            "http://www.fh-regensburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-regensburg.de"
        ],
        "name": "Fachhochschule Regensburg"
    },
    {
        "web_pages": [
            "http://www.fh-reutlingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-reutlingen.de"
        ],
        "name": "Fachhochschule Reutlingen, Hochschule f\u00fcr Technik und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-riedlingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-riedlingen.de"
        ],
        "name": "Deutsch-Ordens Fachhochschule Riedlingen, Hochschule f\u00fcr Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-rosenheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-rosenheim.de"
        ],
        "name": "Fachhochschule Rosenheim, Hochschule f\u00fcr Technik und Wirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-rottenburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-rottenburg.de"
        ],
        "name": "Fachhochschule Rottenburg, Hochschule f\u00fcr Forstwirtschaft"
    },
    {
        "web_pages": [
            "http://www.fh-schmalkalden.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-schmalkalden.de"
        ],
        "name": "Fachhochschule Schmalkalden"
    },
    {
        "web_pages": [
            "http://www.fh-schwaebischhall.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-schwaebischhall.de"
        ],
        "name": "Fachhochschule Schw\u00e4bisch Hall, Hochschule f\u00fcr Gestaltung"
    },
    {
        "web_pages": [
            "http://www.fhs-mannheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhs-mannheim.de"
        ],
        "name": "Fachhochschule Mannheim, Hochschule f\u00fcr Sozialwesen"
    },
    {
        "web_pages": [
            "http://www.fhs-moritzburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhs-moritzburg.de"
        ],
        "name": "Evangelische Fachhochschule f\u00fcr Religionsp\u00e4dagogik, und Gemeindediakonie Moritzburg"
    },
    {
        "web_pages": [
            "http://www.fh-stralsund.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-stralsund.de"
        ],
        "name": "Fachhochschule Stralsund"
    },
    {
        "web_pages": [
            "http://www.fh-telekom-leipzig.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-telekom-leipzig.de"
        ],
        "name": "Deutsche Telekom Fachhochschule Leipzig"
    },
    {
        "web_pages": [
            "http://www.fh-trier.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-trier.de"
        ],
        "name": "Fachhochschule Trier, Hochschule f\u00fcr Technik, Wirtschaft und Gestaltung"
    },
    {
        "web_pages": [
            "http://www.fht-stuttgart.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fht-stuttgart.de"
        ],
        "name": "Fachhochschule Stuttgart, Hochschule f\u00fcr Technik"
    },
    {
        "web_pages": [
            "http://www.fhtw-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhtw-berlin.de"
        ],
        "name": "Fachhochschule f\u00fcr Technik und Wirtschaft Berlin"
    },
    {
        "web_pages": [
            "http://www.hs-ulm.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-ulm.de"
        ],
        "name": "Hochschule Ulm, Hochschule f\u00fcr Angewandte Wissenschaft"
    },
    {
        "web_pages": [
            "http://www.fhvr.berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhvr.berlin.de"
        ],
        "name": "Fachhochschule f\u00fcr Verwaltung und Rechtspflege Berlin"
    },
    {
        "web_pages": [
            "http://www.fhw-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhw-berlin.de"
        ],
        "name": "Fachhochschule f\u00fcr Wirtschaft Berlin"
    },
    {
        "web_pages": [
            "http://www.fh-wedel.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-wedel.de"
        ],
        "name": "Fachhochschule Wedel"
    },
    {
        "web_pages": [
            "http://www.fh-weihenstephan.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-weihenstephan.de"
        ],
        "name": "Fachhochschule Weihenstephan"
    },
    {
        "web_pages": [
            "http://www.fh-weingarten.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-weingarten.de"
        ],
        "name": "Fachhochschule Ravensburg-Weingarten"
    },
    {
        "web_pages": [
            "http://www.fh-westkueste.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-westkueste.de"
        ],
        "name": "Fachhochschule Westk\u00fcste, Hochschule f\u00fcr Wirtschaft und Technik"
    },
    {
        "web_pages": [
            "http://www.fh-wiesbaden.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-wiesbaden.de"
        ],
        "name": "Fachhochschule Wiesbaden"
    },
    {
        "web_pages": [
            "http://www.fh-wolfenbuettel.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-wolfenbuettel.de"
        ],
        "name": "Fachhochschule Braunschweig/Wolfenb\u00fcttel"
    },
    {
        "web_pages": [
            "http://www.fh-worms.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-worms.de"
        ],
        "name": "Fachhochschule Worms"
    },
    {
        "web_pages": [
            "http://www.fhwt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fhwt.de"
        ],
        "name": "Private Fachhochschule f\u00fcr Wirtschaft und Technik Vechta/Diepholz"
    },
    {
        "web_pages": [
            "http://www.fh-wuerzburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-wuerzburg.de"
        ],
        "name": "Fachhochschule W\u00fcrzburg - Schweinfurt"
    },
    {
        "web_pages": [
            "http://www.fh-zwickau.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fh-zwickau.de"
        ],
        "name": "Wests\u00e4chsische Hochschule Zwickau (FH)"
    },
    {
        "web_pages": [
            "http://www.fom.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fom.de"
        ],
        "name": "Fachhochschule f\u00fcr Oekonomie und Management (FOM)"
    },
    {
        "web_pages": [
            "http://www.fu-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "fu-berlin.de"
        ],
        "name": "Freie Universit\u00e4t Berlin"
    },
    {
        "web_pages": [
            "http://www.hanseuni.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hanseuni.de"
        ],
        "name": "Private Hanseuniversit\u00e4t"
    },
    {
        "web_pages": [
            "http://www.hcu-hamburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hcu-hamburg.de"
        ],
        "name": "Hafencity Universit\u00e4t Hamburg"
    },
    {
        "web_pages": [
            "http://www.hdm-stuttgart.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hdm-stuttgart.de"
        ],
        "name": "Fachhochschule Stuttgart, Hochschule der Medien"
    },
    {
        "web_pages": [
            "http://www.hertie-school.org/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hertie-school.org"
        ],
        "name": "Hertie School of Governance"
    },
    {
        "web_pages": [
            "http://www.hfb.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hfb.de"
        ],
        "name": "Hochschule f\u00fcr Bankwirtschaft (HfB), Private Fachhochschule der Bankakademie"
    },
    {
        "web_pages": [
            "http://www.hfg-gmuend.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hfg-gmuend.de"
        ],
        "name": "Fachhochschule Schw\u00e4bisch Gm\u00fcnd, Hochschule f\u00fcr Gestaltung"
    },
    {
        "web_pages": [
            "http://www.hfph.mwn.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hfph.mwn.de"
        ],
        "name": "Hochschule f\u00fcr Philosophie M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.hfp.mhn.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hfp.mhn.de"
        ],
        "name": "Hochschule f\u00fcr Politik (HFP)"
    },
    {
        "web_pages": [
            "http://www.hhl.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hhl.de"
        ],
        "name": "Handelshochschule Leipzig"
    },
    {
        "web_pages": [
            "http://www.himh.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "himh.de"
        ],
        "name": "Hochschule f\u00fcr Internationales Management"
    },
    {
        "web_pages": [
            "http://www.hjs.uni-heidelberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hjs.uni-heidelberg.de"
        ],
        "name": "Hochschule f\u00fcr J\u00fcdische Studien Heidelberg"
    },
    {
        "web_pages": [
            "http://www.hs-albsig.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-albsig.de"
        ],
        "name": "Hochschule Albstadt-Sigmaringen"
    },
    {
        "web_pages": [
            "http://www.hs-anhalt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-anhalt.de"
        ],
        "name": "Hochschule Anhalt (FH), Hochschule f\u00fcr angewandte Wissenschaften"
    },
    {
        "web_pages": [
            "http://www.hs-bremen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-bremen.de"
        ],
        "name": "Hochschule Bremen"
    },
    {
        "web_pages": [
            "http://www.hs-bremerhaven.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-bremerhaven.de"
        ],
        "name": "Hochschule Bremerhaven"
    },
    {
        "web_pages": [
            "http://www.hs-coburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-coburg.de"
        ],
        "name": "Hochschule Coburg"
    },
    {
        "web_pages": [
            "https://www.h-da.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "h-da.de"
        ],
        "name": "Hochschule Darmstadt"
    },
    {
        "web_pages": [
            "http://www.hs-esslingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-esslingen.de"
        ],
        "name": "Hochschule Esslingen"
    },
    {
        "web_pages": [
            "http://www.hs-fulda.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-fulda.de"
        ],
        "name": "Hochschule Fulda"
    },
    {
        "web_pages": [
            "http://www.hs-harz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-harz.de"
        ],
        "name": "Hochschule Harz, Hochschule f\u00fcr angewandte Wissenschaften (FH)"
    },
    {
        "web_pages": [
            "http://www.hs-magdeburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-magdeburg.de"
        ],
        "name": "Hochschule Magdeburg-Stendal (FH)"
    },
    {
        "web_pages": [
            "http://www.hs-wismar.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-wismar.de"
        ],
        "name": "Hochschule Wismar, Fachhochschule f\u00fcr Technik, Wirtschaft und Gestaltung"
    },
    {
        "web_pages": [
            "http://www.hs-zigr.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hs-zigr.de"
        ],
        "name": "Hochschule Zittau/G\u00f6rlitz (FH)"
    },
    {
        "web_pages": [
            "http://www.htw-dresden.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "htw-dresden.de"
        ],
        "name": "Hochschule f\u00fcr Technik und Wirtschaft Dresden (FH)"
    },
    {
        "web_pages": [
            "http://www.htwk-leipzig.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "htwk-leipzig.de"
        ],
        "name": "Hochschule f\u00fcr Technik, Wirtschaft und Kultur Leipzig (FH)"
    },
    {
        "web_pages": [
            "http://www.htwm.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "htwm.de"
        ],
        "name": "Hochschule Mittweida (FH)"
    },
    {
        "web_pages": [
            "http://www.htw-saarland.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "htw-saarland.de"
        ],
        "name": "Hochschule f\u00fcr Technik und Wirtschaft des Saarlandes"
    },
    {
        "web_pages": [
            "http://www.hu-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hu-berlin.de"
        ],
        "name": "Humboldt Universit\u00e4t Berlin"
    },
    {
        "web_pages": [
            "http://www.hwp-hamburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "hwp-hamburg.de"
        ],
        "name": "HWP - Hamburger Universit\u00e4t f\u00fcr Wirtschaft und Politik"
    },
    {
        "web_pages": [
            "http://www.ihi-zittau.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ihi-zittau.de"
        ],
        "name": "Internationales Hochschulinstitut Zittau"
    },
    {
        "web_pages": [
            "http://www.international.fh-aalen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "international.fh-aalen.de"
        ],
        "name": "Internationale Fachhochschule Aalen"
    },
    {
        "web_pages": [
            "http://www.ism-dortmund.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ism-dortmund.de"
        ],
        "name": "International School of Management ISM Dortmund"
    },
    {
        "web_pages": [
            "http://www.isnm.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "isnm.de"
        ],
        "name": "International School of New Media, University of L\u00fcbeck"
    },
    {
        "web_pages": [
            "http://www.i-u.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "i-u.de"
        ],
        "name": "International University in Germany"
    },
    {
        "web_pages": [
            "http://www.jacobs-university.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "jacobs-university.de"
        ],
        "name": "Jacobs University Bremen"
    },
    {
        "web_pages": [
            "http://www.karlshochschule.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "karlshochschule.de"
        ],
        "name": "Karlshochschule International University"
    },
    {
        "web_pages": [
            "http://www.kath-fh-nord.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kath-fh-nord.de"
        ],
        "name": "Katholische Fachhochschule Norddeutschland"
    },
    {
        "web_pages": [
            "http://www.kfb-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kfb-berlin.de"
        ],
        "name": "Katholische Fachhochschule Berlin (KFB)"
    },
    {
        "web_pages": [
            "http://www.kfh-Freiburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kfh-Freiburg.de"
        ],
        "name": "Katholische Fachhochschule Freiburg, Hochschule f\u00fcr Sozialwesen, Religionsp\u00e4dagogik und Pflege"
    },
    {
        "web_pages": [
            "http://www.kfh-mainz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kfh-mainz.de"
        ],
        "name": "Katholische Fachhochschule Mainz"
    },
    {
        "web_pages": [
            "http://www.kfhnw.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kfhnw.de"
        ],
        "name": "Katholische Fachhochschule Nordrhein-Westfalen"
    },
    {
        "web_pages": [
            "http://www.kh-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kh-berlin.de"
        ],
        "name": "Kunsthochschule Berlin-Weissensee, Hochschule f\u00fcr Gestaltung"
    },
    {
        "web_pages": [
            "http://www.khsa.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "khsa.de"
        ],
        "name": "Katholische Hochschule f\u00fcr Soziale Arbeit Saarbr\u00fccken"
    },
    {
        "web_pages": [
            "http://www.ksfh.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ksfh.de"
        ],
        "name": "Katholische Stiftungsfachhochschule M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.ku-eichstaett.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ku-eichstaett.de"
        ],
        "name": "Katholische Universit\u00e4t Eichst\u00e4tt"
    },
    {
        "web_pages": [
            "http://www.kunstakademie-duesseldorf.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kunstakademie-duesseldorf.de"
        ],
        "name": "Kunstakademie D\u00fcsseldorf."
    },
    {
        "web_pages": [
            "http://www.merkur-fh.org/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "merkur-fh.org"
        ],
        "name": "Merkur Internationale FH Karlsruhe"
    },
    {
        "web_pages": [
            "http://www.merz-akademie.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "merz-akademie.de"
        ],
        "name": "Merz Akademie, Hochschule f\u00fcr Gestaltung Stuttgart"
    },
    {
        "web_pages": [
            "http://www.mfh-iserlohn.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "mfh-iserlohn.de"
        ],
        "name": "M\u00e4rkische Fachhochschule Iserlohn"
    },
    {
        "web_pages": [
            "http://www.mh-hannover.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "mh-hannover.de"
        ],
        "name": "Medizinische Hochschule Hannover"
    },
    {
        "web_pages": [
            "http://www.mh-trossingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "mh-trossingen.de"
        ],
        "name": "Staatliche Hochschule f\u00fcr Musik"
    },
    {
        "web_pages": [
            "http://www.mu-luebeck.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "mu-luebeck.de"
        ],
        "name": "Medizinische Universit\u00e4t L\u00fcbeck"
    },
    {
        "web_pages": [
            "http://www.muthesius.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "muthesius.de"
        ],
        "name": "Muthesius-Hochschule, Fachhochschule f\u00fcr Kunst und Gestaltung"
    },
    {
        "web_pages": [
            "http://www.nordakademie.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "nordakademie.de"
        ],
        "name": "Nordakademie, Staatlich anerkannte private Fachhochschule mit dualen Studieng\u00e4ngen"
    },
    {
        "web_pages": [
            "http://www.paderborn.de/theofak/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "paderborn.de"
        ],
        "name": "Theologische Fakult\u00e4t Paderborn"
    },
    {
        "web_pages": [
            "http://www.pfh-goettingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "pfh-goettingen.de"
        ],
        "name": "Private Fachhochschule G\u00f6ttingen"
    },
    {
        "web_pages": [
            "http://www.ph-erfurt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ph-erfurt.de"
        ],
        "name": "P\u00e4dagogische Hochschule Erfurt/M\u00fchlhausen"
    },
    {
        "web_pages": [
            "http://www.ph-freiburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ph-freiburg.de"
        ],
        "name": "P\u00e4dagogische Hochschule Freiburg"
    },
    {
        "web_pages": [
            "http://www.ph-gmuend.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ph-gmuend.de"
        ],
        "name": "P\u00e4dagogische Hochschule Schw\u00e4bisch Gm\u00fcnd"
    },
    {
        "web_pages": [
            "http://www.ph-heidelberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ph-heidelberg.de"
        ],
        "name": "P\u00e4dagogische Hochschule Heidelberg"
    },
    {
        "web_pages": [
            "http://www.philtheol-augustin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "philtheol-augustin.de"
        ],
        "name": "Philosophisch-Theologische Hochschule SVD Sankt Augustin"
    },
    {
        "web_pages": [
            "http://www.ph-karlsruhe.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ph-karlsruhe.de"
        ],
        "name": "P\u00e4dagogische Hochschule Karlsruhe"
    },
    {
        "web_pages": [
            "http://www.ph-ludwigsburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ph-ludwigsburg.de"
        ],
        "name": "P\u00e4dagogische Hochschule Ludwigsburg"
    },
    {
        "web_pages": [
            "http://www.ph-weingarten.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ph-weingarten.de"
        ],
        "name": "P\u00e4dagogische Hochschule Weingarten"
    },
    {
        "web_pages": [
            "http://www.popakademie.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "popakademie.de"
        ],
        "name": "Popakademie Baden-W\u00fcrttemberg"
    },
    {
        "web_pages": [
            "http://www.privatfh-da.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "privatfh-da.de"
        ],
        "name": "Private FernFachhochschule Darmstadt"
    },
    {
        "web_pages": [
            "http://www.pth-bb.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "pth-bb.de"
        ],
        "name": "Philosophisch-Theologische Hochschule der Salesianer Don Boscos"
    },
    {
        "web_pages": [
            "http://www.pth-muenster.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "pth-muenster.de"
        ],
        "name": "Philosophisch-Theologische Hochschule M\u00fcnster"
    },
    {
        "web_pages": [
            "http://www.pthv.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "pthv.de"
        ],
        "name": "Philosophisch-Theologische Hochschule Vallendar der Gesellschaft des Katholischen Apostolates (Pallottiner)"
    },
    {
        "web_pages": [
            "http://www.rauheshaus.de/fachhochschule/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "rauheshaus.de"
        ],
        "name": "Evangelische Fachhochschule f\u00fcr Sozialp\u00e4dagogik der \"Diakonenanstalt des Rauhen Hauses\" Hamburg"
    },
    {
        "web_pages": [
            "http://www.rfh-koeln.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "rfh-koeln.de"
        ],
        "name": "Rheinische Fachhochschule K\u00f6ln"
    },
    {
        "web_pages": [
            "http://www.ruhr-uni-bochum.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "ruhr-uni-bochum.de"
        ],
        "name": "Ruhr-Universit\u00e4t Bochum"
    },
    {
        "web_pages": [
            "http://www.rwth-aachen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "rwth-aachen.de"
        ],
        "name": "Rheinisch Westf\u00e4lische Technische Hochschule Aachen"
    },
    {
        "web_pages": [
            "http://www.selk.de/LThH/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "selk.de"
        ],
        "name": "Lutherische Theologische Hochschule Oberursel"
    },
    {
        "web_pages": [
            "http://www.siewerth-akademie.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "siewerth-akademie.de"
        ],
        "name": "Gustav-Siewerth-Akademie"
    },
    {
        "web_pages": [
            "http://www.siu-heidelberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "siu-heidelberg.de"
        ],
        "name": "Schiller International University, Heidelberg"
    },
    {
        "web_pages": [
            "http://www.srh-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "srh-berlin.de"
        ],
        "name": "SRH University of Applied Sciences"
    },
    {
        "web_pages": [
            "http://www.st-georgen.uni-frankfurt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "st-georgen.uni-frankfurt.de"
        ],
        "name": "Philosophisch-Theologische Hochschule Sankt Georgen"
    },
    {
        "web_pages": [
            "http://www.stw.de/shb/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "stw.de"
        ],
        "name": "Steinbeis-Hochschule-Berlin"
    },
    {
        "web_pages": [
            "http://www.tfh-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tfh-berlin.de"
        ],
        "name": "Technische Fachhochschule Berlin"
    },
    {
        "web_pages": [
            "http://www.tfh-bochum.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tfh-bochum.de"
        ],
        "name": "Technische Fachhochschule Georg Agricola f\u00fcr Rohstoff, Energie und, Umwelt zu Bochum"
    },
    {
        "web_pages": [
            "http://www.tfh-wildau.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tfh-wildau.de"
        ],
        "name": "Technische Fachhochschule Wildau"
    },
    {
        "web_pages": [
            "http://www.thh-friedensau.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "thh-friedensau.de"
        ],
        "name": "Theologische Hochschule Friedensau"
    },
    {
        "web_pages": [
            "http://www.tiho-hannover.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tiho-hannover.de"
        ],
        "name": "Tier\u00e4rztliche Hochschule Hannover"
    },
    {
        "web_pages": [
            "http://www.tu-berlin.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-berlin.de"
        ],
        "name": "Technische Universit\u00e4t Berlin"
    },
    {
        "web_pages": [
            "http://www.tu-bs.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-bs.de"
        ],
        "name": "Technische Universit\u00e4t Carolo-Wilhelmina Braunschweig"
    },
    {
        "web_pages": [
            "http://www.tu-chemnitz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-chemnitz.de"
        ],
        "name": "Technische Universit\u00e4t Chemnitz"
    },
    {
        "web_pages": [
            "http://www.tu-clausthal.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-clausthal.de"
        ],
        "name": "Technische Universit\u00e4t Clausthal"
    },
    {
        "web_pages": [
            "http://www.tu-cottbus.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-cottbus.de"
        ],
        "name": "Brandenburgische Technische Universit\u00e4t Cottbus"
    },
    {
        "web_pages": [
            "https://www.tu-darmstadt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-darmstadt.de"
        ],
        "name": "Technische Universit\u00e4t Darmstadt"
    },
    {
        "web_pages": [
            "http://www.tu-dresden.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-dresden.de"
        ],
        "name": "Technische Universit\u00e4t Dresden"
    },
    {
        "web_pages": [
            "http://www.tu-freiberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-freiberg.de"
        ],
        "name": "Technische Universit\u00e4t Bergakademie Freiberg"
    },
    {
        "web_pages": [
            "http://www.tu-harburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-harburg.de"
        ],
        "name": "Technische Universit\u00e4t Hamburg-Harburg"
    },
    {
        "web_pages": [
            "http://www.tu-ilmenau.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tu-ilmenau.de"
        ],
        "name": "Technische Universit\u00e4t Ilmenau"
    },
    {
        "web_pages": [
            "http://www.tum.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "tum.de",
            "tum.edu"
        ],
        "name": "Technische Universit\u00e4t M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.uni-augsburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-augsburg.de"
        ],
        "name": "Universit\u00e4t Augsburg"
    },
    {
        "web_pages": [
            "http://www.uni-bamberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-bamberg.de"
        ],
        "name": "Otto-Friedrich Universit\u00e4t Bamberg"
    },
    {
        "web_pages": [
            "http://www.uni-bayreuth.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-bayreuth.de"
        ],
        "name": "Universit\u00e4t Bayreuth"
    },
    {
        "web_pages": [
            "http://www.uni-bielefeld.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-bielefeld.de"
        ],
        "name": "Universit\u00e4t Bielefeld"
    },
    {
        "web_pages": [
            "http://www.uni-bonn.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-bonn.de"
        ],
        "name": "Rheinische Friedrich-Wilhelms Universit\u00e4t Bonn"
    },
    {
        "web_pages": [
            "http://www.uni-bremen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-bremen.de"
        ],
        "name": "Universit\u00e4t Bremen"
    },
    {
        "web_pages": [
            "http://www.unibw-hamburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "unibw-hamburg.de"
        ],
        "name": "Universit\u00e4t der Bundeswehr Hamburg"
    },
    {
        "web_pages": [
            "http://www.unibw-muenchen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "unibw-muenchen.de"
        ],
        "name": "Universit\u00e4t der Bundeswehr M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.uni-dortmund.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-dortmund.de"
        ],
        "name": "Universit\u00e4t Dortmund"
    },
    {
        "web_pages": [
            "http://www.uni-duesseldorf.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-duesseldorf.de"
        ],
        "name": "Heinrich-Heine Universit\u00e4t D\u00fcsseldorf"
    },
    {
        "web_pages": [
            "http://www.uni-duisburg-essen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-duisburg-essen.de"
        ],
        "name": "Universit\u00e4t Duisburg-Essen"
    },
    {
        "web_pages": [
            "http://www.uni-erfurt.de/phil-theol/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-erfurt.de"
        ],
        "name": "Philosophisch-Theologisches Studium Erfurt, Staatlich anerkannte Wissenschaftliche Hochschule"
    },
    {
        "web_pages": [
            "http://www.uni-erfurt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-erfurt.de"
        ],
        "name": "Universit\u00e4t Erfurt"
    },
    {
        "web_pages": [
            "http://www.uni-erlangen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-erlangen.de"
        ],
        "name": "Friedrich-Alexander Universit\u00e4t Erlangen-N\u00fcrnberg"
    },
    {
        "web_pages": [
            "http://www.uni-flensburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-flensburg.de"
        ],
        "name": "Universit\u00e4t Flensburg"
    },
    {
        "web_pages": [
            "http://www.uni-frankfurt.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-frankfurt.de"
        ],
        "name": "Johann Wolfgang Goethe Universit\u00e4t Frankfurt am Main"
    },
    {
        "web_pages": [
            "http://www.uni-freiburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-freiburg.de"
        ],
        "name": "Albert-Ludwigs-Universit\u00e4t Freiburg"
    },
    {
        "web_pages": [
            "http://www.uni-giessen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-giessen.de"
        ],
        "name": "Justus Liebig Universit\u00e4t Gie\u00dfen"
    },
    {
        "web_pages": [
            "http://www.uni-goettingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-goettingen.de"
        ],
        "name": "Georg-August Universit\u00e4t G\u00f6ttingen"
    },
    {
        "web_pages": [
            "http://www.uni-greifswald.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-greifswald.de"
        ],
        "name": "Ernst-Moritz-Arndt Universit\u00e4t Greifswald"
    },
    {
        "web_pages": [
            "http://www.uni-halle.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-halle.de"
        ],
        "name": "Martin-Luther Universit\u00e4t Halle-Wittenberg"
    },
    {
        "web_pages": [
            "http://www.uni-hamburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-hamburg.de"
        ],
        "name": "Universit\u00e4t Hamburg"
    },
    {
        "web_pages": [
            "http://www.uni-hannover.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-hannover.de"
        ],
        "name": "Universit\u00e4t Hannover"
    },
    {
        "web_pages": [
            "http://www.uni-heidelberg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-heidelberg.de"
        ],
        "name": "Ruprecht-Karls-Universit\u00e4t Heidelberg"
    },
    {
        "web_pages": [
            "http://www.uni-hildesheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-hildesheim.de"
        ],
        "name": "Universit\u00e4t Hildesheim"
    },
    {
        "web_pages": [
            "http://www.uni-hohenheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-hohenheim.de"
        ],
        "name": "Universit\u00e4t Hohenheim"
    },
    {
        "web_pages": [
            "http://www.uni-jena.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-jena.de"
        ],
        "name": "Friedrich-Schiller Universit\u00e4t Jena"
    },
    {
        "web_pages": [
            "http://www.kit.edu/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "kit.edu"
        ],
        "name": "Karlsruher Institut f\u00fcr Technologie"
    },
    {
        "web_pages": [
            "http://www.uni-kassel.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-kassel.de"
        ],
        "name": "Universit\u00e4t Kassel"
    },
    {
        "web_pages": [
            "http://www.uni-kiel.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-kiel.de"
        ],
        "name": "Christian-Albrechts-Universit\u00e4t Kiel"
    },
    {
        "web_pages": [
            "http://www.uni-kl.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-kl.de"
        ],
        "name": "Universit\u00e4t Kaiserslautern"
    },
    {
        "web_pages": [
            "http://www.uni-koblenz-landau.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-koblenz-landau.de"
        ],
        "name": "Universit\u00e4t Koblenz-Landau"
    },
    {
        "web_pages": [
            "http://www.uni-koeln.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-koeln.de"
        ],
        "name": "Universit\u00e4t K\u00f6ln"
    },
    {
        "web_pages": [
            "http://www.uni-konstanz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-konstanz.de"
        ],
        "name": "Universit\u00e4t Konstanz"
    },
    {
        "web_pages": [
            "http://www.uni-leipzig.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-leipzig.de"
        ],
        "name": "Universit\u00e4t Leipzig"
    },
    {
        "web_pages": [
            "http://www.uni-lueneburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-lueneburg.de"
        ],
        "name": "Universit\u00e4t L\u00fcneburg"
    },
    {
        "web_pages": [
            "http://www.uni-magdeburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-magdeburg.de"
        ],
        "name": "Otto-von-Guericke Universit\u00e4t Magdeburg"
    },
    {
        "web_pages": [
            "http://www.uni-mainz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-mainz.de"
        ],
        "name": "Johannes-Gutenberg Universit\u00e4t Mainz"
    },
    {
        "web_pages": [
            "http://www.uni-mannheim.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-mannheim.de"
        ],
        "name": "Universit\u00e4t Mannheim"
    },
    {
        "web_pages": [
            "http://www.uni-marburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-marburg.de"
        ],
        "name": "Phillips-Universit\u00e4t Marburg"
    },
    {
        "web_pages": [
            "http://www.uni-muenchen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-muenchen.de"
        ],
        "name": "Ludwig-Maximilians-Universit\u00e4t M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.lmu.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "lmu.de"
        ],
        "name": "Ludwig-Maximilians-Universit\u00e4t M\u00fcnchen"
    },
    {
        "web_pages": [
            "http://www.uni-muenster.de/",
            "http://www.wwu.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-muenster.de",
            "wwu.de"
        ],
        "name": "Westf\u00e4lische Wilhelms-Universit\u00e4t M\u00fcnster"
    },
    {
        "web_pages": [
            "http://www.uni-oldenburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-oldenburg.de"
        ],
        "name": "Carl von Ossietzky Universit\u00e4t Oldenburg"
    },
    {
        "web_pages": [
            "http://www.uni-osnabrueck.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-osnabrueck.de"
        ],
        "name": "Universit\u00e4t Osnabr\u00fcck"
    },
    {
        "web_pages": [
            "http://www.uni-paderborn.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-paderborn.de"
        ],
        "name": "Universit\u00e4t Paderborn"
    },
    {
        "web_pages": [
            "http://www.uni-passau.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-passau.de"
        ],
        "name": "Universit\u00e4t Passau"
    },
    {
        "web_pages": [
            "http://www.uni-potsdam.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-potsdam.de"
        ],
        "name": "Universit\u00e4t Potsdam"
    },
    {
        "web_pages": [
            "http://www.uni-polsdam.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-polsdam.de"
        ],
        "name": "Universit\u00e4t Polsdam"
    },
    {
        "web_pages": [
            "http://www.uni-regensburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-regensburg.de"
        ],
        "name": "Universit\u00e4t Regensburg"
    },
    {
        "web_pages": [
            "http://www.uni-rostock.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-rostock.de"
        ],
        "name": "Universit\u00e4t Rostock"
    },
    {
        "web_pages": [
            "http://www.uni-saarland.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-saarland.de"
        ],
        "name": "Universit\u00e4t des Saarlandes"
    },
    {
        "web_pages": [
            "http://www.uni-siegen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-siegen.de"
        ],
        "name": "Universit\u00e4t Siegen"
    },
    {
        "web_pages": [
            "http://www.uni-stuttgart.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-stuttgart.de"
        ],
        "name": "Universit\u00e4t Stuttgart"
    },
    {
        "web_pages": [
            "http://www.uni-trier.de/uni/theo/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-trier.de"
        ],
        "name": "Theologische Fakult\u00e4t Trier"
    },
    {
        "web_pages": [
            "http://www.uni-trier.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-trier.de"
        ],
        "name": "Universit\u00e4t Trier"
    },
    {
        "web_pages": [
            "http://www.uni-tuebingen.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-tuebingen.de"
        ],
        "name": "Eberhard-Karls-Universit\u00e4t T\u00fcbingen"
    },
    {
        "web_pages": [
            "http://www.uni-ulm.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-ulm.de"
        ],
        "name": "Universit\u00e4t Ulm"
    },
    {
        "web_pages": [
            "http://www.uni-vechta.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-vechta.de"
        ],
        "name": "Hochschule Vechta"
    },
    {
        "web_pages": [
            "http://www.uni-weimar.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-weimar.de"
        ],
        "name": "Bauhaus Universit\u00e4t Weimar"
    },
    {
        "web_pages": [
            "http://www.uni-wh.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-wh.de"
        ],
        "name": "Private Universit\u00e4t Witten/Herdecke"
    },
    {
        "web_pages": [
            "http://www.uni-wuerzburg.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-wuerzburg.de"
        ],
        "name": "Bayerische Julius-Maximilians-Universit\u00e4t W\u00fcrzburg"
    },
    {
        "web_pages": [
            "http://www.uni-wuppertal.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-wuppertal.de"
        ],
        "name": "Bergische Universit\u00e4t Gesamthochschule Wuppertal"
    },
    {
        "web_pages": [
            "http://www.uni-wuppertal.de/inst/kiho/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "uni-wuppertal.de"
        ],
        "name": "Kirchliche Hochschule Wuppertal"
    },
    {
        "web_pages": [
            "http://www.whu-koblenz.de/"
        ],
        "alpha_two_code": "DE",
        
        "country": "Germany",
        "domains": [
            "whu-koblenz.de"
        ],
        "name": "Wissenschaftliche Hochschule f\u00fcr Unternehmensf\u00fchrung, Otto-Beisheim Hochschule"
    },
    {
        "web_pages": [
            "http://www.dhbw-mannheim.de/"
        ],
        "alpha_two_code": "DE",
        "state-province": "null",
        "country": "Germany",
        "domains": [
            "dhbw-mannheim.de"
        ],
        "name": "Duale Hochschule Baden-Wuerttemberg Mannheim"
    }
]
)
```
result:
```
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 309,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
```

# Step 2 - read data
* get all info:
```javascript
db.countryInfo.find()
```
result:
```
{ "_id" : ObjectId("5c29d115b7f9e9c751065a7f"), "name" : "Israel", "topLevelDomain" : [ ".il" ], "alpha2Code" : "IL", "alpha3Code" : "ISR", "callingCodes" : [ "972" ], "capital" : "Jerusalem", "altSpellings" : [ "IL", "State of Israel", "Medīnat Yisrā'el" ], "region" : "Asia", "subregion" : "Western Asia", "population" : 8527400, "latlng" : [ 31.5, 34.75 ], "demonym" : "Israeli", "area" : 20770, "gini" : 39.2, "timezones" : [ "UTC+02:00" ], "borders" : [ "EGY", "JOR", "LBN", "SYR" ], "nativeName" : "יִשְׂרָאֵל", "numericCode" : "376", "currencies" : [ { "code" : "ILS", "name" : "Israeli new shekel", "symbol" : "₪" } ], "languages" : [ { "iso639_1" : "he", "iso639_2" : "heb", "name" : "Hebrew (modern)", "nativeName" : "עברית" }, { "iso639_1" : "ar", "iso639_2" : "ara", "name" : "Arabic", "nativeName" : "العربية" } ], "flag" : "https://restcountries.eu/data/isr.svg", "regionalBlocs" : [ ], "cioc" : "ISR" }
{ "_id" : ObjectId("5c29d115b7f9e9c751065a80"), "name" : "Germany", "topLevelDomain" : [ ".de" ], "alpha2Code" : "DE", "alpha3Code" : "DEU", "callingCodes" : [ "49" ], "capital" : "Berlin", "altSpellings" : [ "DE", "Federal Republic of Germany", "Bundesrepublik Deutschland" ], "region" : "Europe", "subregion" : "Western Europe", "population" : 81770900, "latlng" : [ 51, 9 ], "demonym" : "German", "area" : 357114, "gini" : 28.3, "timezones" : [ "UTC+01:00" ], "borders" : [ "AUT", "BEL", "CZE", "DNK", "FRA", "LUX", "NLD", "POL", "CHE" ], "nativeName" : "Deutschland", "numericCode" : "276", "currencies" : [ { "code" : "EUR", "name" : "Euro", "symbol" : "€" } ], "languages" : [ { "iso639_1" : "de", "iso639_2" : "deu", "name" : "German", "nativeName" : "Deutsch" } ], "flag" : "https://restcountries.eu/data/deu.svg", "regionalBlocs" : [ { "acronym" : "EU", "name" : "European Union", "otherAcronyms" : [ ], "otherNames" : [ ] } ], "cioc" : "GER" }
```


* get all info in nice format:
```javascript
db.countryInfo.find().pretty()
```
result:
```
{
        "_id" : ObjectId("5c29d115b7f9e9c751065a7f"),
        "name" : "Israel",
        "topLevelDomain" : [
                ".il"
        ],
        "alpha2Code" : "IL",
        "alpha3Code" : "ISR",
        "callingCodes" : [
                "972"
        ],
        "capital" : "Jerusalem",
        "altSpellings" : [
                "IL",
                "State of Israel",
                "Medīnat Yisrā'el"
        ],
        "region" : "Asia",
        "subregion" : "Western Asia",
        "population" : 8527400,
        "latlng" : [
                31.5,
                34.75
        ],
        "demonym" : "Israeli",
        "area" : 20770,
        "gini" : 39.2,
        "timezones" : [
                "UTC+02:00"
        ],
        "borders" : [
                "EGY",
                "JOR",
                "LBN",
                "SYR"
        ],
        "nativeName" : "יִשְׂרָאֵל",
        "numericCode" : "376",
        "currencies" : [
                {
                        "code" : "ILS",
                        "name" : "Israeli new shekel",
                        "symbol" : "₪"
                }
        ],
        "languages" : [
                {
                        "iso639_1" : "he",
                        "iso639_2" : "heb",
                        "name" : "Hebrew (modern)",
                        "nativeName" : "עברית"
                },
                {
                        "iso639_1" : "ar",
                        "iso639_2" : "ara",
                        "name" : "Arabic",
                        "nativeName" : "العربية"
                }
        ],
        "flag" : "https://restcountries.eu/data/isr.svg",
        "regionalBlocs" : [ ],
        "cioc" : "ISR"
}
{
        "_id" : ObjectId("5c29d115b7f9e9c751065a80"),
        "name" : "Germany",
        "topLevelDomain" : [
                ".de"
        ],
        "alpha2Code" : "DE",
        "alpha3Code" : "DEU",
        "callingCodes" : [
                "49"
        ],
        "capital" : "Berlin",
        "altSpellings" : [
                "DE",
                "Federal Republic of Germany",
                "Bundesrepublik Deutschland"
        ],
        "region" : "Europe",
        "subregion" : "Western Europe",
        "population" : 81770900,
        "latlng" : [
                51,
                9
        ],
        "demonym" : "German",
        "area" : 357114,
        "gini" : 28.3,
        "timezones" : [
                "UTC+01:00"
        ],
        "borders" : [
                "AUT",
                "BEL",
                "CZE",
                "DNK",
                "FRA",
                "LUX",
                "NLD",
                "POL",
                "CHE"
        ],
        "nativeName" : "Deutschland",
        "numericCode" : "276",
        "currencies" : [
                {
                        "code" : "EUR",
                        "name" : "Euro",
                        "symbol" : "€"
                }
        ],
        "languages" : [
                {
                        "iso639_1" : "de",
                        "iso639_2" : "deu",
                        "name" : "German",
                        "nativeName" : "Deutsch"
                }
        ],
        "flag" : "https://restcountries.eu/data/deu.svg",
        "regionalBlocs" : [
                {
                        "acronym" : "EU",
                        "name" : "European Union",
                        "otherAcronyms" : [ ],
                        "otherNames" : [ ]
                }
        ],
        "cioc" : "GER"
}
```
* Select a specific field (in our case - we want to select the "cioc" field):
```javascript
db.countryInfo.find({},{"cioc":1})
```
result:
```
{ "_id" : ObjectId("5c29d115b7f9e9c751065a7f"), "cioc" : "ISR" }
{ "_id" : ObjectId("5c29d115b7f9e9c751065a80"), "cioc" : "GER" }
```
* Select a specific field without the "_id"(in our case - we want to select the "cioc" field)
```javascript
db.countryInfo.find({},{"cioc":1,"_id":0})
```
result:
```
{ "cioc" : "ISR" }
{ "cioc" : "GER" }
```
* Select only this : "region","subregion", "area" 
```javascript
db.countryInfo.find({},{"region":1,"subregion":1,"area":1,"_id":0})
```
result:
```
{ "region" : "Asia", "subregion" : "Western Asia", "area" : 20770 }
{ "region" : "Europe", "subregion" : "Western Europe", "area" : 357114 }
```
* Select the number of the documents in the collection
```javascript
db.countryInfo.find().count()
```
result:
```
2
```
* Select the number of the documents in the collection, that returns true to the given condition: (in our case - find how many universities we have in israel)
```javascript
db.uniInfo.find({"country": "Israel"}).count()
```
result:
```
22
```


* Select documents by condition (in this case - we want to select the countries that have in "region" the value "Asia", and have in the "population" the value 8527400):
```javascript
db.countryInfo.find({"region": "Asia", "population": 8527400})
```
result:
```
{ "_id" : ObjectId("5c29d115b7f9e9c751065a7f"), "name" : "Israel", "topLevelDomain" : [ ".il" ], "alpha2Code" : "IL", "alpha3Code" : "ISR", "callingCodes" : [ "972" ], "capital" : "Jerusalem", "altSpellings" : [ "IL", "State of Israel", "Medīnat Yisrā'el" ], "region" : "Asia", "subregion" : "Western Asia", "population" : 8527400, "latlng" : [ 31.5, 34.75 ], "demonym" : "Israeli", "area" : 20770, "gini" : 39.2, "timezones" : [ "UTC+02:00" ], "borders" : [ "EGY", "JOR", "LBN", "SYR" ], "nativeName" : "יִשְׂרָאֵל", "numericCode" : "376", "currencies" : [ { "code" : "ILS", "name" : "Israeli new shekel", "symbol" : "₪" } ], "languages" : [ { "iso639_1" : "he", "iso639_2" : "heb", "name" : "Hebrew (modern)", "nativeName" : "עברית" }, { "iso639_1" : "ar", "iso639_2" : "ara", "name" : "Arabic", "nativeName" : "العربية" } ], "flag" : "https://restcountries.eu/data/isr.svg", "regionalBlocs" : [ ], "cioc" : "ISR" }
```

* Select a specific field from documents by condition (in this case - we want to select the field "name" only the countries that have in "region" the value "Asia", and have in the "population" the value 8527400):
```javascript
db.countryInfo.find({"region": "Asia", "population": 8527400},{ "_id" :0, "name" :1})
```
result:
```
{ "name" : "Israel" }
``` 
