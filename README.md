Sample Exocortex Scenarios... constructs, as I think of them.

This repository contains a selected subset of my Huginn agent networks that are in production at this time.  They are some of my simplest and earliest constructs to serve as examples of how Huginn agent networks should be structured so that they're easy to understand, debug, and maintain.

I give my agent networks persona-like names so that I can remember what they do easily.  You don't have to be this idiosyncratic.

I put the name of the scenario in the title of each constituent agent as an aid to debugging, because sometimes I forget to associate agents with scenarios.

Where applicable, each scenario's agents use the {% credential foo... %} construct, which substitutes sensitive values (like API keys) so they don't have to be hardcoded.

By default, Email Digest and Email Agents send messages to the default e-mail address Huginn is configured for.  There are a few agents that are configured to contact example e-mail addresses to show how it's done.

The sample scenarios are:
* Butterfly In China - An agent network that polls the weather and air quality forecasts for cities I routinely travel to for work.  Please note that before this scenario will successfully import, you must have created a credential called ''weather_underground_api_key'' on the Credentials screen.
* Searcherizer - A construct that mimics the functionality of Google Alerts using Searx and sentiment analysis.
* Shake, Rattle, and Roll - A construct that polls the United States Geological Service's seismographic monitoring network for tectonic activity stronger than a 4.0 on the Richter scale every few minutes and e-mails alerts if a reasonably strong earthquake is detected.  A Manual Agent for testing beeper.io connectivity is included for no good reason.
* Test Scenario - A construct that shows you how to program agents that interact with REST APIs.
* Tripwire - A set of RSS Agents that check FBI Most Wanted Lists (and an Archive) for changes every morning.
* Twitter Activity Monitor - A construct that demonstrates how to scan the Twitter Activity Stream for arbitrary keywords and build email reports from what it finds.
* Mastodon Integration Demo - A very small agent network that posts events to a [Mastodon](https://joinmastodon.org/) instance.
* Elephant - A small agent network that backs up posts on the Fediverse into separate files on the host running Huginn.  Requires that insecure agents be enabled so it will have access to the file system.
* Test Matrix Integration - A proof-of-concept agent network for interfacing Huginn with a [Matrix](https://matrix.org/) server.
* Searx Answering API Examples - A collection of agents that demonstrate how to interact with [Searx's](https://searx.me/) answerers using the JSON API.

