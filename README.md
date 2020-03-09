# Raspberry Pi with arduino 
## workup for an asset-tracker


Use Raspberry Pi to connect via usb to Arduino with Grove Shield and 
[Grove GPS sensor](http://wiki.seeedstudio.com/Grove-GPS/)

![arduino uno and grove hat](images/uno-grove-sheild.png)
***Arduino Uno with Grove GPS sensor attached***

usb to raspberry pi v2

to get GPS and location information

to add grab Temp, Humidity and Accelerometer data ...


Need to signup for Mapquest Developer account and get an API key

```bash
export MAPQUEST_KEY=hw26Ajxxxxxxxxxxx
```

in `python3 code gps.py` it will call 

Mapquest get url to

`http://www.mapquestapi.com/geocoding/v1/reverse?key=MAPQUESTKEY&location=40.72817333333333,-73.98259166666666&includeRoadMetadata=true&includeNearestIntersection=true`


and returns something similar to
```json
'nearestIntersection': {   'distanceMeters': '151.78865',
                            'label': 'E '
                                    '11th '
                                    'St '
                                    '& '
                                    'Avenue '
                                    'C',
                            'latLng': {   'latitude': 41.72785,
                                            'longitude': -73.982223},
                            'streetDisplayName': 'Avenue '
                                                'C'},
    'postalCode': '10009-4XXX',
    'sideOfStreet': 'L'
}

```

### resources

convert grove gps data to meanigful information
https://github.com/Knio/pynmea2

