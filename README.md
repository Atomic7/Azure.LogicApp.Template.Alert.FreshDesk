![Nodinite](./assets/images/Nodinite_logo_payoff2line_w195.png)
# Nodinite - Webhook - Logic App FreshDesk Template

[![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

Ever wanted to integrate [Nodinite](https://nodinite.com/) with [Freshdesk](https://freshdesk.com/)? Using [Nodinite's](https://nodinite.com) HTTP WebHook plugin and a Logic App it is possible. 

This repository contains an Azure ARM template that can receive an HTTP call from [Nodinite](https://nodinite.com) and uses Azure's built-in connector for [FreshDesk](https://freshdesk.com/).

## What it does

![Azure Logic App Designer](./assets/images/azure-logic-app-designer-screenshot.png)

The Logic app will be configured to retrieve data from Nodinite (the JSON schema is automatically provided) and loops over all Monitor Views that have a changed state. The Logic App will automatically create new tickets in your freshdesk for each Monitor View that has a status code that does not match 0 (status code for OK).

Some fields are pre-defined:

* Description
* Priority
* Status 
* Subject
* Type

Depending on your FreshDesk instance, other fields might need to be configured, e.g. **Product**.