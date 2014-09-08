ngPrayTimes
===========


# Injecting
Inject it by:

```
angular
  .module('beautifulprayerApp', [
    ...,
    'ngPrayTimes'
  ])
```

Then in your controller:

```
.controller(function(prayTimes){
	praytimes = new prayTimes()
})
```
# Usage

###Calculating times:
```
prayTimes.getTimes(date, [lat, lng], timezoneOffset, dst, format) // Will return the times in a json 
// Example
prayTimes.getTimes(new Date(), [43, -80], -5) 
```

###Setting the method to calculate:
```
prayTimes.setMethod(method)
```
Methods: 
Method	Description
MWL:	Muslim World League
ISNA:	Islamic Society of North America
Egypt:	Egyptian General Authority of Survey
Makkah:	Umm al-Qura University, Makkah
Karachi:	University of Islamic Sciences, Karachi
Tehran:	Institute of Geophysics, University of Tehran
Jafari:	Shia Ithna Ashari (Ja`fari)


###Adjusting methods:
Pass a json for needed adjustments. Example:

```
prayTimes.adjust( { asr: 'Hanafi'} )
```

#More information
See [official documentation]



[official documentation]:http://praytimes.org/wiki/Code_Manual

