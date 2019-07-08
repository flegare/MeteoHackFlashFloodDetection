# MeteoHackFlashFloodDetection

This project allow detection of potential flash flood and send alerts. The system rely on realtime and forecast of Environment and Climate Change Canada rain forecast combined with hydrological water sheds stations. The current project only work on area covered by ECCC (TODO: Put links of station map)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Data feed used: 

* Capabilities of the HRDPS layer 
https://geo.weather.gc.ca/geomet/?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetCapabilities&LAYERS=HRDPS.CONTINENTAL_PR

* List of capabilities
https://geo.weather.gc.ca/geomet?lang=en&service=WCS&version=2.0.1&request=GetCapabilities

* Query rain forecast of a coordonate :
https://geo.weather.gc.ca/geomet/?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetFeatureInfo&QUERY_LAYERS=HRDPS.CONTINENTAL_PR&INFO_FORMAT=text/plain&i=5&j=5&EXCEPTIONS=xml&LAYERS=HRDPS.CONTINENTAL_PR&CRS=EPSG:4326&BBOX=45.50,-73.56,45.51,-73.55&WIDTH=10&HEIGHT=10&TIME=2019-07-09T19:00:00Z

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* A big thanks to Vincent Fortin of ECCC for the support and inspiration!
