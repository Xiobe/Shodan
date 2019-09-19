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
