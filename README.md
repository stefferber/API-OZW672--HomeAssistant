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
1.) Create helper entities in *Settings->Helpers* custom entities *input_number* and *input_select* with Values *Automatic*, *Comfort*, *Reduced*. In my case are entities *input_number.nastaveni_teploty_kotle* = *input_number.settings_temperature_boiler*, *input_number.utlumova_teplota_kotle* = *input_number.attenuating_temperature_boiler* , *input_select.kotel_druh_provozu* = *input_select.boiler_operation_type*    
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/entities.jpg)  
2.) Add to *configuration.yaml* helpers entities and API strings -> see configuration.yaml 

3.) Add automations -> see automations.yaml..

# Result
![](https://github.com/vencakratky/API-OZW672--HomeAssistant/blob/master/Result.jpg)
