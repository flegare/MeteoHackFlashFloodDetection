# MeteoHackFlashFloodDetection

This project was done during the METEOHACK 2019. (https://www.hackworks.com/en/meteohack)  allow detection of potential flash flood in part of Canada and determine if there is a risk for a specific watershed. The system rely on real time and forecast of Environment and Climate Change Canada rain forecast combined with hydrological watersheds stations and historical data. The current project only work using the water level stations covered by ECCC (see map here: https://bit.ly/2LJ7zL5). 

## Flash flood problem in Canada

From 1900 to 2013, there have been 289 flood disasters across Canada. That is more than snowstorms, hail and wildfire combined, securing flooding in the number one spot for the most costly of natural disasters in Canada in terms of property damage. In fact, 50 percent of disaster-related compensation payments made by insurance companies are for flood damage.

For the federal government, Federal payments under Disaster Financial Assistance for Floods have totaled over $713 million dollars since 1970.

The top 5 most expensive floods in Canada this century are:

Southern Alberta Flooding June 2013 ($5 billion)
Red River Flood ($1 billion)
Assiniboine River ($1 billion)
Southern Ontario 2005 ($587 million)
Edmonton Flood 2004 ($303 million)

With such huge numbers at stake, it comes as no surprise that the government, home insurance providers and property owners have become very interested in the topic of how to mitigate flood risk. [Source: https://www.squareoneinsurance.com/water-flood-damage-in-canada]

While we can’t control the weather, we can certainly work to minimize damage from floods caused by weather. This project intent to help detect conditions that would cause flash floods. By combining weather forecast and current state of watersheds.  A better way to detect these flash floods prior they occur could help city manager and citizens prepare for these drastic events and reduce health risks and damage to property. 


## How we determine the conditions of a flash flood

To determine if we are in an exceptional condition we will use the following formula :

Qo + Qt Qmax
 
Where:

Qo: The actual flow of the watershed updated every 5 min. in meters cube per seconds.

Qt =f ( Ptotal  Wa)

Qt is a function that takes the total of precipitation for the watershed (Ptotal) multiplied by the total area of the watershed (Wa).

We define the total of precipitation with the following formula:

 Ptotal = (P past +P forecasted ) -S

Where :

P past : Total of past precipitation for the are for the last X hours in millimeters.

P forecasted : Total of forecasted precipitation for the are for the next 48 hours in millimeters.

S: The runoff curve number that define the empirical soil water retention for the area. In this case we will use the following constant for all watersheds. 

This could be improved by using this data set at later points : https://daac.ornl.gov/cgi-bin/dsviewer.pl?ds_id=1566

S =1000CN-10 with CN equal to 65, so S =  5.38
 

Qmax: The maximum flow for of the watershed of the past 20 years event.




## Getting Started
TBC



### Prerequisites

Python
Android SDK

### Installing

TBC



## Data feed used: 

* Capabilities of the HRDPS layer 
https://geo.weather.gc.ca/geomet/?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetCapabilities&LAYERS=HRDPS.CONTINENTAL_PR

* List of capabilities
https://geo.weather.gc.ca/geomet?lang=en&service=WCS&version=2.0.1&request=GetCapabilities

* Query rain forecast of a coordonate :
https://geo.weather.gc.ca/geomet/?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetFeatureInfo&QUERY_LAYERS=HRDPS.CONTINENTAL_PR&INFO_FORMAT=text/plain&i=5&j=5&EXCEPTIONS=xml&LAYERS=HRDPS.CONTINENTAL_PR&CRS=EPSG:4326&BBOX=45.50,-73.56,45.51,-73.55&WIDTH=10&HEIGHT=10&TIME=2019-07-09T19:00:00Z

* Water shed definition
https://dd.weather.gc.ca/analysis/precip/hrdpa_watershed/shapefile/06/

* Actual flow of a station
https://dd.weather.gc.ca/hydrometric/csv/ON/daily/

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* A big thanks to Vincent Fortin of ECCC for the support and inspiration!


