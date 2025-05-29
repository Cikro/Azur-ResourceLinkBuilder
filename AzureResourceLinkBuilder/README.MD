# Azure Resource Link Builder
## Overview
At my place of work, we have begun adding `Deployment Slots` to our Azure App Services. 
I currently use the Azure Portal to navigate from all resources, into a specific Azure Web App,
And then into the specific deployment slot. From There, I can then access the Deployment Log from the
Deployment Center, or Application Insights for that specific slot.
This is a pain because it requires multiple clicks and lots of time waiting for the webpage to load.

I discovered that the Azure Portal has access to Dashboards that can have widgets and graphs and things.
While there is no widget to display Deployment Slots, there is a Markdown widget.

With the Markdown widget, I can create a table of links to each of the Azure Web App's deployment slots.
This will save me the load time, the clicking and some sanity. It should also allow me to 
share the Dashboard with my team, so they can also benefit from it.

## PLan
1. Fetch the list of Azure Web Apps from a specific Resource Group.
2. Fetch the list of Deployment Slots for each Azure Web App.
3. filter the Deployment Slots to only include those that follow a specific naming convention.
4. Find the Application Insights resource for each Deployment Slot.
5. Generate a Markdown table with links to each Deployment Slot and its Application Insights resource.
