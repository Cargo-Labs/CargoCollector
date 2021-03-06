CargoCollector
==============

Android service that interfaces with car via a standard ELM327 compatable OBD-II reader.

Data points are gathered from the car and various sensors on the mobile phone on an interval and/or as changes occur.  These data points are marshalled to JSON, compressed, and sent to an attached ZeroMQ server on a set interval.

###Data Points
- Location (GPS/A-GPS)
- Vehicle Speed (MPH)
- Engine Temperature (&deg;F)
- Fuel Efficiency (MPG)

###Sample JSON
```json
{
  "location": {
      "lat": 123.456789,
      "lng": 123.456789,
      "timestamp": 1234567890
  },
  "timestamp": 1234567890,
  "speed": 45.2,
  "engine_temp": 202.3,
  "mpg": 23.53
}
```
