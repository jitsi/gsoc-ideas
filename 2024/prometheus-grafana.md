# Prometheus scraping and Grafana dashboards

## Description

The [docker-jitsi-meet](https://github.com/jitsi/docker-jitsi-meet) project provides an easy way for the 
[Jitsi Meet](https://github.com/jitsi/jitsi-meet) system to be deployed.
The underlying components expose various metrics, but while we've seen many custom solutions for metrics 
aggregation and monitoring over the years, none of them are standard or easy to instrument. This makes monitoring 
a Jitsi Meet system for usage (e.g. number of conferences), stress (e.g. memory use), and troubleshooting 
service-level events hard.

This project aims to solve that problem by providing a new docker container which collects metrics from
the different Jitsi Meet components, and [Grafana](https://grafana.com/grafana/dashboards/) dashboard templates for dysplaing the data.

A [previous GSoC project](https://summerofcode.withgoogle.com/archive/2022/projects/CtgpJGaV) went a long way towards
providing metrics in a common interface using [Prometheus](https://prometheus.io/). 


## Expected outcomes
* Create a new docker container, which is deployed alongside [docker-jitsi-meet](https://github.com/jitsi/docker-jitsi-meet),
and collects and saves Prometheus metrics from the different components.

* Create various templates for Grafana dashboards for monitoring.

## Skills / Technologies

Docker, Prometheus, Grafana.

## Possible mentors

Aaron van Meerten, Scott Boone, Boris Grozev, Saúl Ibarra Corretgé, Lucian-Paul Torje

## Expected project size

Medium (175 hours) or Large (350 hours)

## Difficulty

Medium
