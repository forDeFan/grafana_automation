<h1>Dockerized Grafana Dashboard</h1>

Automatically generates predefined dashboard with API fed panels for currency exchange rates in PLN at last year (USD, GBP) as well as gold price and inflation rates.<br>
Dashboard calls to open (no key or auth needed) API of NBP (National Bank of Poland) and json generated data endpoint (inflation rates) from investing.com

<h2>Technologies used</h2>
* Grafana 7.1<br>
* Docker<br>
* Docker-compose<br>


### Prerequisites

* Docker and docker-compose installed


### Install & Run

```
$ git clone https://github.com/forDeFan/grafana_automation.git
$ cd grafana_automation
$ docker-compose up -d --build
```

If persistent data needed - uncomment lines on docker-compose.yml and:

```
$ docker volume create --name=grafana-data
$ docker-compose up -d --build
```

After succesfull build Grafana dashboard available at:
http://localhost:9000/
