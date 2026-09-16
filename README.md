# Rei Fantasy Assistant

Rei Fantasy Assistant is a personal, single-user conversational interface for accessing Yahoo Fantasy Sports information through the official Yahoo Fantasy Sports API.

Rei is part of Project Presence, an experimental locally hosted AI assistant that uses natural voice interaction to help its user access information and operate connected services.

## Intended Yahoo Fantasy functionality

The initial integration will provide read-only access to the authorized user’s own Yahoo Fantasy Football account. Rei will be able to retrieve and summarize:

* Fantasy leagues and teams
* Team rosters
* Weekly matchups and scores
* League standings
* Player information
* Injury and availability information provided by Yahoo
* Schedule and bye-week information available through the API

Example requests include:

* “Which Yahoo Fantasy leagues am I in?”
* “Who am I playing this week?”
* “What is my current score?”
* “Show me my roster.”
* “Where am I in the standings?”
* “Which players on my team are injured or on a bye?”

## Access model

This project is intended for:

* Personal use
* A single authorized Yahoo user
* Non-commercial use
* Read-only Fantasy Sports access
* Locally hosted operation

The initial version will not:

* Change starting lineups
* Add or drop players
* Submit waiver claims
* Propose or accept trades
* Modify league settings
* Perform any other write transaction

## Authentication and security

Rei uses Yahoo OAuth 2.0. The user signs in directly through Yahoo and authorizes the application without providing a Yahoo password to Rei.

Security principles include:

* OAuth credentials are not stored in this repository
* Access and refresh tokens remain local
* Secrets are excluded from source control
* OAuth state values are validated
* Access is limited to the minimum functionality required
* Fantasy information is not sold or shared
* The application does not request access to Yahoo email or contacts
* Yahoo credentials and tokens are not sent to the AI model

## Data handling

Fantasy data is requested only when needed to answer the authorized user’s question. The prototype does not operate a public user database and does not provide access to other users’ private Yahoo information.

## Current status

The local OAuth 2.0 authorization-code flow has been implemented successfully. Yahoo Fantasy Sports API access is pending approval through the Yahoo Sports Developer Portal.

## Contact

This repository provides a public project overview for Yahoo’s API review process. The application itself remains a private, locally hosted personal prototype.
