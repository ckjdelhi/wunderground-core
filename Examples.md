[downloads](downloads.md)

# Examples #

the following examples shows how to use wunderground-core api to getting
weather data from a wunderground weather station:

## Simple use a HttpDataReaderService in Java application ##

```

// create a instance of a wunderground data reader
HttpDataReaderService dataReader = new HttpDataReaderService();

// select a wunderground weather station (ID "INORDRHE72" = Dortmund-Mengede)
WeatherStation weatherStation = WeatherStations.ALL.get("INORDRHE72");

// set selected weather station to data reader
dataReader.setWeatherStation(weatherStation);

// get current (last) weather data set from selected station
DataSet current = dataReader.getCurrentData();

// print selected weather station ID
System.out.println(weatherStation.getStationId());

// print city, state and country of weather station
System.out.println(weatherStation.getCity() + " " + weatherStation.getState() + " " + weatherStation.getCountry());

// print datetime of measure and temperature ...
System.out.println(current.getDateTime() + " " + current.getTemperature());

```

## Find out all weather stations of a country by using WeatherStationService ##

```
// create an instance of WeatherStationService
WeatherStationService weatherStationService = new WeatherStationService();

// find all weather stations
List<WeatherStation> stations = weatherStationService.findAllWeatherStationsByCountry("Germany");

// iterate over all founded weather stations and write some information to stdout
for (WeatherStation weatherStation : stations) {
    System.out.println(weatherStation.getStationId() + "\t" + "\t" + weatherStation.getCity() + 
         "\t" + weatherStation.getCountry());		
}
```

## Fetch weather data by given date (release 1.0.2) ##

```
// set desired date ...
Date weatherDate = new DateTime(2011, 8, 15, 0, 0, 0).toDate();

// create an instance of HttpDataReaderService
HttpDataReaderService dataReader = new HttpDataReaderService();

// set desired weather station ...
dataReader.setWeatherStation(WeatherStations.INOORDBR35_BOXMEER);   	

// set desired date to HttpDataReaderService
dataReader.setWeatherDate(weatherDate);

// investigate minimum temperature of desired day ...
DataSet minTemp = this.httpDataReaderService.minTemperature();
    	
// investigate maximum temperature of desired day ...
DataSet maxTemp = this.httpDataReaderService.maxTemperature();
```

## connections through a http proxy server (since release 1.0.5) ##

```
// create HttpProxy object and set proxy data
HttpProxy proxy = new HttpProxy();
proxy.setUrl("my-proxy-server-url");
proxy.setPort(8080);
proxy.setUsername("me");
proxy.setPassword("secret");

// create HttpDataReaderService
HttpDataReaderService dataReader = new HttpDataReaderService();

// assign HttpProxy object to data reader
dataReader.setHttpProxy(proxy);

// do something ...
DataSet current = dataReader.getCurrentData();
```

## fetch wheater data by given month and year (since release 1.0.6) ##

```
// create an instance of HttpDataReaderService
HttpDataReaderService dataReader = new HttpDataReaderService();

// set graphspan to "month"
dataReader.setDataGraphSpan(DataGraphSpan.MONTH);

// set desired mont and year as DateTime (february 2012)
dataReader.setWeatherDate(new DateTime(2012, 2, 1, 0, 0, 0).toDate());

List<DataSet> monthly = dataReader.readDataSets();
for (DataSet dataSet : monthly) {
   System.out.println(dataSet.getDateTime() + "\t" + dataSet.getTemperatureHigh() 
         + "\t" + dataSet.getTemperatureLow());
}
```