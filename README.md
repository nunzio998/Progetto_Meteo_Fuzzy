# Progetto_Meteo_Fuzzy
## Variabili
- ### Pressione Atmosferica
    E' stato considerato un intervallo tra 970 e 1045 HPa per il territorio preso in esame.

    _https://www.meteogiuliacci.it/curiosit%C3%A0/record-storici-incredibili-di-alta-pressione-italia-e-europa_

    _https://www.meteotorre.it/record.php_
- ### Temperatura
    E' stato considerato un intervallo tra -10 e 40° centrato in 15° ± 10°.

    _https://www.meteotorre.it/record.php_

    _https://it.climate-data.org/europa/italia/lazio-416/_
- ### Probabilità di precipitazione
- ### Umidità
    E' stato considerato un intervallo medio centrato in 72%.

    _https://it.climate-data.org/europa/italia/lazio/roma-1185/_
- ### Velocità del vento
    E' stato considerato massimo di 120 Km/h.

    _https://www.meteotorre.it/record.php_
    
## Regole
- Se il barometro segna valori sotto 1000 hPa è probabile che il tempo volga al brutto, specie con umidità oltre 70%.

  _https://www.meteogiuliacci.it/curiosit%C3%A0/record-storici-incredibili-di-alta-pressione-italia-e-europa_
- Se il barometro segna valori oltre 1025 hPa,  il tempo tende al bello, specie con umidità sotto al 60%.

    _https://www.meteogiuliacci.it/curiosit%C3%A0/record-storici-incredibili-di-alta-pressione-italia-e-europa_


Le regole che sono state inserite sono state derivate principalmente da
quattro regole generali, ognuna delle quali si riferisce ad uno dei quattro 
risultati possibili della previsione.

- Temporale:
[Pressione: bassa | Temperatura: bassa/media/alta | Probabilità_precipitazione: alta
| Umidita: alta | Vento: forte/ molto_forte]

- Pioggia:
[Pressione: bassa/media | Temperatura: bassa/media/alta | Probabilità_precipitazione: media/alta
| Umidita: media/alta | Vento: lieve/medio/forte]

- Nuvoloso:
[Pressione: bassa/media | Temperatura: bassa/media/alta | Probabilità_precipitazione: alta
| Umidita: media/alta | Vento: lieve/medio/forte]

che semplificata è:
[Pressione: not(alta) | Temperatura: bassa/media/alta | Probabilità_precipitazione: not(bassa)
| Umidita: not(bassa) | Vento: not(molto_forte)]

- Sereno:
[Pressione: bassa/media | Temperatura: bassa/media/alta | Probabilità_precipitazione: bassa
| Umidita: bassa/media/alta | Vento: lieve/medio/forte/molto_forte]

che semplificata:
[Pressione: not(bassa) | Temperatura: bassa/media/alta | Probabilità_precipitazione: bassa
| Umidita: bassa/media/alta | Vento: lieve/medio/forte/molto_forte]
