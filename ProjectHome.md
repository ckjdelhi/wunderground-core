# Welcome! #

<h3>NEW!</h3>
<b><u>Version 2.0.0 of wunderground Java API released!</u></b>
<p>the 1.0.x version branch is not further developed. The 2.0.0 relase is a complete redesign of the API. The new version is ready for use on mobile devices!</p>
<p>Have look on new project website with a Ajax Live Demo as SpringMVC webapplication:</p>
<a href='http://www.jartist.de/wunderground-java-api-live-demo-ajax/'>wunderground-core 2.0.0 project site</a>
<p>You can download the jar distribution from there ...</p>
<br />


&lt;hr/&gt;


<br />
<b>implemented feature in release 1.0.6:</b>
<br />
<ul>
<li>
fetch weather data for a wheater station by given month and year  -> see last <a href='https://code.google.com/p/wunderground-core/wiki/Examples'>examples</a>
</li>
<li>
all JUnit tests run sucessful<br>
</li>
<li>
additional javadoc jar -> see <a href='https://code.google.com/p/wunderground-core/downloads/list'>Downloads</a> section<br>
</li>
</ul>
<b><u>implemented function since release 1.0.2/1.0.5:</u></b>
<br />
<ul>
<li>
<i>fetch weather data history by given date in HttpDataReaderService (as yet it was only possible to get weather data for current day -> see <a href='https://code.google.com/p/wunderground-core/wiki/Examples'>examples</a>)</i>
</li>
<li>
<i>full support for connections through a http proxy server -> see <a href='https://code.google.com/p/wunderground-core/wiki/Examples'>examples</a>)</i>
</li>
</ul>

### Project description ###

the wunderground-core project provides a Java API for accessing and processing public weather data from http://www.wunderground.com.
These data can be used to build own desktop, web or console application. Attributable to listener support it can be used to create alerts to inform you when defined conditions are fullfilled. Much more use cases are possible.

This time it is only possible to get weather data for the current day. It is planned to
implement data handling for month, years an any other days.

You can get the current release from <a href='https://code.google.com/p/wunderground-core/downloads/list'>Downloads</a> section.
For knowing bugs and planned features take a look in <a href='https://code.google.com/p/wunderground-core/issues/list'>issue tracker</a>.
In addtion how to use API you can find some example in project <a href='https://code.google.com/p/wunderground-core/wiki/Examples'>Wiki</a>.


&lt;hr/&gt;


### Current features ###

  * read data directly from via HTTP request
  * read data from a local file
  * implement own data reader
  * data listener support
  * implement own listeners
  * investigate actual weather values
  * investigate minimum and maximum temperature of current day
  * investigate minimum and maximum dewpoint of current day
  * fetching all weather stations by given country
  * console application in own project <a href='https://code.google.com/p/wunderground-console/'>wunderground-console</a>
  * fetch weather data history by given date
  * connections through a proxy server
  * weather data handling for years, month and other days like "today"

### Planned features ###
  * AJAX support for web-based applications
  * different statistics tools
  * database support for weather data and weather stattions


&lt;hr/&gt;





