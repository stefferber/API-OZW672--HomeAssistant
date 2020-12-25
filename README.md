# API-OZW672--HomeAssistant

Czech - for English see below
## Api připojení webového serveru Siemens OZW672 s aplikací Home Assistant
...Doporučuji nejprve otestovat komunikaci v lokální síti přes api webové rozhraní kotle na adrese:   
http://192.168.X.X/main.app?SessionID=****YourSessionafterlogin***&Section=webapi  
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/webapi.jpg)  
## Návod
1.) Vytvořit v *Nastavení->Pomocníci* pomocné entity *input_number* a *input_select* s hodnotami *automatický*, *Komfortní*, *Útlum*. V mém případě jsou to entity *input_number.nastaveni_teploty_kotle*, *input_number.utlumova_teplota_kotle*, *input_select.kotel_druh_provozu*  
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/entities.jpg)  
2.) Přidat do *configuration.yaml* pomocné entity a API řetězce -> viz soubory  
3.) Přidat do *automations.yaml* automatizace -> viz soubory   

# Výsledek 
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/Result.jpg)


## Api connecting the Siemens OZW672 web server with the application Home Assistant 
...I recommend little playing with webapi interface in your local network (after login to OZW):    
http://192.168.X.X/main.app?SessionID=****YourSessionafterlogin***&Section=webapi  
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/webapi.jpg)  
## Instructions   
1.) Create helper entities in *Settings->Helpers* custom entities *input_number* and *input_select* with Values *Automatic*, *Comfort*, *Reduced*. In my case are entities *input_number.nastaveni_teploty_kotle* = *input_number.boiler_temp_settings*, *input_number.utlumova_teplota_kotle* = *input_number.boiler_temp_attenuating* , *input_select.kotel_druh_provozu* = *input_select.boiler_operation_type*    
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/entities.jpg)  
2.) Add to *configuration.yaml* helpers entities and API strings -> see configuration.yaml 

3.) Add automations -> see automations.yaml..

# Result
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/Result.jpg)

# Mapping Table

This mapping is for OZW672 Version 6 with Brötje SB120C and using [Brötje "System-Handbuch ISR-Plus"](https://polo.broetje.de/pdf/systemhandbuch_isr.pdf) as of 01.09.2009. P# is the Brötje "Parameter" and Web ID is the REST identifier.

|P#  |German Name                                   |Alternative German Name                |Standard Value|Web ID|Home Assistant name            |Comment|
|----|----------------------------------------------|---------------------------------------|--------------|------|-------------------------------|-------|
|712 |Raumtemperatur Reduziertsollwert Heizkreis 1  |Reduziertsollwert                      |16            |957   |boiler_temp_settings_reduced   |       |
|714 |Raumtemperatur Frostschutzsollwert Heizkreis 1|                                       |10            |958   |                               |       |
|720 |Heizkennlinie 1 Steilheit                     |                                       |1,5           |959   |boiler_heating_curve           |       |
|721 |Heizkennlinien-Parallelverschiebung           |Kennlinie Verschiebung                 |0             |960   |                               |       |
|726 |Heizkennlinie Adaption Heizkreis 1            |                                       |0             |961   |                               |       |
|1610|Trinkwassertemperatur-Nennsollwert            |Nennsollwert                           |55            |1006  |boiler_temp_DHW_setpoint       |       |
|1612|Trinkwassertemperatur-Reduziertsollwert       |Reduziertsollwert                      |40            |1007  |                               |       |
|8000|Status Heizkreis 1                            |                                       |0             |1160  |boiler_status_heating_circuit_1|       |
|8001|Status Heizkreis 2                            |                                       |0             |1161  |boiler_status_heating_circuit_2|       |
|8003|Status Trinkwasser                            |                                       |0             |1162  |boiler_status_DHW              |       |
|8005|Status Kessel                                 |                                       |              |1163  |boiler_status                  |       |
|8310|Kesseltemperatur-Istwert                      |                                       |              |1166  |                               |       |
|8310|Kesseltemperatur-Istwert                      |                                       |              |1219  |boiler_temp                    |       |
|8314|Rücklauftemperatur-Istwert                    |                                       |              |1168  |boiler_temp_return             |       |
|8700|Aussentemperatur                              |                                       |              |?     |                               |       |
|8703|Aussentemperatur gedämpft                     |                                       |0             |1182  |                               |       |
|8704|Aussentemperatur gemischt                     |                                       |0             |1183  |boiler_temp_outside            |       |
|8740|Raumtemperatur 1 Istwert                      |Raumtemperatur 1                       |20            |1230  |boiler_temp_room               |       |
|8741|Raumtemperatur Komfortsollwert Heizkreis 1    |Komfortsollwert                        |20            |956   |boiler_temp_settings_comfort   |       |
|8741|Raumtemperatur-Sollwert Aktuell               |Raumsollwert 1                         |20            |1231  |                               |       |
|8743|Vorlauftemperatur Istwert Heizkreis 1         |                                       |60            |1232  |boiler_temp_supply             |       |
|8761|Heizkreismischer 2 Auf                        |                                       |0             |?     |                               |       |
|8762|Heizkreismischer 2 Zu                         |                                       |0             |?     |                               |       |
|8765|Drehzahl Heizkreispumpe 2                     |                                       |0             |?     |                               |       |
|8795|Drehzahl Heizkreispumpe P                     |                                       |0             |?     |                               |       |
|8820|Trinkwasserpumpe Q3                           |                                       |0             |?     |                               |       |
|8825|Drehzahl Trinkwasserpumpe                     |                                       |0             |?     |                               |       |
|8830|Trinkwassertemperatur-Istwert Oben (B3)       |Trinkwassertemperatur 1                |0             |1193  |                               |       |
|8830|Trinkwassertemperatur-Istwert Oben (B3)       |Trinkwassertemperatur 1                |0             |1220  |boiler_temp_DHW                |       |
|8831|Trinkwassersollwert                           |Brauchwassertemperatur-Sollwert aktuell|55            |1194  |                               |       |
|N.A.|Fehlermeldung                                 |                                       |              |1216  |boiler_error_message           |       |
