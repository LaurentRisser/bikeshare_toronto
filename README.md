How to see the flows of bikes in the Bike Share Toronto Service
Does bike share go round trip or one way?

The purpose of this notebook is to analyse the flow of bikes. Are bikes returned to its initial location? Or are there flows of bike from one region to another?

The sum of all the travels for each station for one year are too noisy, so

Data can be split between weekend days or not
Stations can be grouped by proximity in order to define regions
Data can be summarized by period of time ( Day, Week , Month, Year)
Focus on 2018, that should be enough representative
Graph representation :

A node is a station or a region
A edge is the sum of all travel between 2 nodes during a period of time
For each node we consider the balance between outgoing and incoming flows
To simplify : a travel from one station to the same station is not taken in account. (balance is zero)
To simplify : the inverse edges are grouped as follow, (10 travels from 1 to 2 and 12 travels from 2 to 1, gives -2 travels from 1 to 2) (5 travels from 1 to 2 and 4 travels from 2 to 1, gives +1 travels from 1 to 2)
The plan

Get the stations information
Load the data
Clustering of the stations in 20 regions
