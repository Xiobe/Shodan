# Shodan

Shodan is a search engine build for searching systems online. It can help you with investigating you in a defensive and offensive way.

## Shodan for defense

### Searching on IP
The simplest use is just to log in and search for IP addresses you own. It will return you a page with more information if it has something on that IP address.

```
$ nslookup www.belgium.be
Name:	www.belgium.be
Address: 193.191.245.244
```
This will return the page https://www.shodan.io/host/193.191.245.244. You will see which open ports Shodan discovered.

What we actually did was use a shortcut for the filter ```ip:"193.191.245.244"```. Filters is where the power is in any search engine.

### Searching for malware
If you want to create a list of all malware instances Shodan detected in order to protect your organization you can use the filter ```category:malware```.  We can combine this with other filters for example if we want to know which malware was detected for Belgium we can set the filter to ```category:malware country:be```. Since Belgium is a tiny country the results are not spectacular but try ```category:malware country:us,ru,br```. This filter combines the US, Russia an Brazil. They are big so it is only logical to find more.

This allows us to create a map of "The united malware of Europe" with the search terms ```category:"malware" country:"at,be,bg,hr,cy,cz,dk,ee,fi,fr,de,gr,hu,ie,it,lv,lt,lu,mt,nl,pl,pt,ro,sk,si,es,se,uk"```

### Searching for industrial control systems (ics)

#### Modbus
Modbus is a protocol for ics, it provides you with raw access to the control system without requiring any authentication. It means that if you have your systems in the result set you have an issue.

To search for modbus devices search for ```port:502```

## Shodan for offense

### Searching on IP
The simplest use is just to log in and search for IP addresses you own. It will return you a page with more information if it has something on that IP address.

```
$ nslookup www.belgium.be
Name:	www.belgium.be
Address: 193.191.245.244
```
This will return the page https://www.shodan.io/host/193.191.245.244. You will see which open ports Shodan discovered.

What we actually did was use a shortcut for the filter ```ip:"193.191.245.244"```. Filters is where the power is in any search engine.

### Searching for industrial control systems (ics)

#### Modbus
Modbus is a protocol for ics, it provides you with raw access to the control system without requiring any authentication. It means that if you have your systems in the result set you have an issue.

To search for modbus devices search for ```port:502```

## Shodan filters
This is a summary of filters

### Generic filters

| Name        | Description           | Type  | Example  |
| ------------- |:-------------| :-----| :-----|
| ip      | Searches for the IP address of a specific host | string | ```ip:"193.191.245.244"``` |
| country      | Searches for a specific country | string | ```country:"be"``` |

### Specialized filters

| Name        | Description           | Type  | Example  |
| ------------- |:-------------| :-----| :-----|
| catergory:"malware"      | Searches for malware | string | ```category:"malware"``` |
