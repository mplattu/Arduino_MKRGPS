# Arduino MKR GPS library

## Methods

### `begin()`

Initialize the GPS.

#### Syntax 

```
GPS.begin()
GPS.begin(mode)
```

#### Parameters

`GPS_MODE_I2C` to use the MKR GPS with the I2C cable (default setting), `GPS_MODE_SHIELD` if using the MKR GPS as a shield.

#### Returns

1 on success, 0 on failure.

#### Example

```
if (!GPS.begin()) {
    Serial.println("Failed to initialize the GPS!");
    while(1);
}
```

#### See also

* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `end()`

De-initialize the GPS.

#### Syntax 

```
GPS.end()
```

#### Parameters

None.

#### Returns

Nothing.

#### Example

```
if (!GPS.begin()) {
    Serial.println("Failed to initialize the GPS!");
    while(1);
}

// Read GPS data here...

// Done working with the GPS
GPS.end();
```

#### See also

* [begin()](#begin)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `available()`

Query if new GPS data is available().

#### Syntax 

```
GPS.available()
```

#### Parameters

None.

#### Returns

0 if no new GPS data is available, 1 if new GPS data is available.

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS data
    float latitude = GPS.latitude();
    float longitude = GPS.longitude();
    float altitude = GPS.altitude();
    float speed = GPS.speed();
    int satellites = GPS.satellites();

    // ...
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `latitude()`

Read the latitude of the GPS.

#### Syntax 

```
GPS.latitude()
```

#### Parameters

None.

#### Returns

GPS latitude in degrees.

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS data
    float latitude = GPS.latitude();
    float longitude = GPS.longitude();

    // ...

    // Print GPS data
    Serial.print("Location: ");
    Serial.print(latitude, 7);
    Serial.print(", ");
    Serial.println(longitude, 7);
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `longitude()`

Read the latitude of the GPS.

#### Syntax 

```
GPS.latitude()
```

#### Parameters

None.

#### Returns

GPS longitude in degrees.

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS data
    float latitude = GPS.latitude();
    float longitude = GPS.longitude();

    // ...

    // Print GPS data
    Serial.print("Location: ");
    Serial.print(latitude, 7);
    Serial.print(", ");
    Serial.println(longitude, 7);
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `speed()`

Read the ground speed of the GPS.

#### Syntax 

```
GPS.speed()
```

#### Parameters

None.

#### Returns

GPS ground speed in km/h. 

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS data
    float speed = GPS.speed();

    // ...

    // Print GPS data
    Serial.print("Ground speed: ");
    Serial.print(speed);
    Serial.println(" km/h");
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `course()`

Read the course of the GPS.

#### Syntax 

```
GPS.course()
```

#### Parameters

None.

#### Returns

GPS course in degrees. 

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS data
    float course = GPS.course();

    // ...

    // Print GPS data
    Serial.print("Course: ");
    Serial.print(course);
    Serial.println(" degrees");
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `variation()`

Read the magnetic variation of the GPS.

#### Syntax 

```
GPS.variation()
```

#### Parameters

None.

#### Returns

GPS magnetic variation in degrees.

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS data
    float variation = GPS.variation();

    // ...

    // Print GPS data
    Serial.print("Variation: ");
    Serial.print(variation);
    Serial.println(" degrees");
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `altitude()`

Read the altitude of the GPS.

#### Syntax 

```
GPS.altitude()
```

#### Parameters

None.

#### Returns

GPS altitude in meters. 

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS data
    float altitude = GPS.altitude();

    // ...

    // Print GPS data
    Serial.print("Altitude: ");
    Serial.print(altitude);
    Serial.println("m");
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `satellites()`

Read the number of satellites being tracked by the GPS.

#### Syntax 

```
GPS.satellites()
```

#### Parameters

None.

#### Returns

The number of satellites being tracked by the GPS.

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS values
    int satellites = GPS.satellites();

    // ...

    // Print GPS data
    Serial.print("Number of satellites: ");
    Serial.println(satellites);
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `satellites()`

Read the number of satellites being tracked by the GPS.

#### Syntax 

```
GPS.satellites()
```

#### Parameters

None.

#### Returns

The number of satellites being tracked by the GPS.

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS values
    int satellites = GPS.satellites();

    // ...

    // Print GPS data
    Serial.print("Number of satellites: ");
    Serial.println(satellites);
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [getTime()](#gettime)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `getTime()`

Read the current epoch time from the GPS.

#### Syntax 

```
GPS.getTime()
```

#### Parameters

None.

#### Returns

The current epoch time from the GPS.

#### Example

```
// Check if there is new GPS data available
if (GPS.available()) {
    // Read GPS values
    unsigned long epochTime = GPS.getTime();

    // ...

    // Print GPS data
    Serial.print("Epoch time: ");
    Serial.println(epochTime);
}
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [standby()](#standby)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `standby()`

Put the GPS in standby mode.

#### Syntax 

```
GPS.standby()
```

#### Parameters

None.

#### Returns

None.

#### Example

```
// Put the GPS in standby mode
Serial.println("Standby mode");
GPS.standby();

// Wait for 10 seconds
delay(10000);

// Wake up the GPS
Serial.println("Wakeup");
GPS.wakeup();

// Wait for new GPS data to become available
Serial.print("Waiting new location data... ");
while (!GPS.available());

// ...
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [wakeup()](#wakeup)
* [setUpdateRate()](#setupdaterate)

### `wakeup()`

Wake up the GPS from standby mode.

#### Syntax 

```
GPS.wakeup()
```

#### Parameters

None.

#### Returns

None.

#### Example

```
// Put the GPS in standby mode
Serial.println("Standby mode");
GPS.standby();

// Wait for 10 seconds
delay(10000);

// Wake up the GPS
Serial.println("Wakeup");
GPS.wakeup();

// Wait for new GPS data to become available
Serial.print("Waiting new location data... ");
while (!GPS.available());

// ...
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [setUpdateRate()](#setupdaterate)

### `setUpdateRate()`

Sends new update rates to GPS module.

#### Syntax 

```
GPS.setUpdateRate(measRate, navRate, timeRef)
```

#### Parameters

* `uint16_t measRate` - The elapsed time between GNSS
measurements, which defines the rate, e.
g. 100 ms => 10 Hz, 1000 ms => 1 Hz,
10000 ms => 0.1 Hz. Measurement rate
should be greater than or equal to 25 ms. Unit: ms.
* `uint16_t navRate` - The ratio between the number of
measurements and the number of
navigation solutions, e.g. 5 means five
measurements for every navigation
solution. Maximum value is 127. Unit: cycles.
* `uint16_t timeRef` - The time system to which measurements
are aligned: (0: UTC time, 1: GPS time). Unit: -.

For more information about the parameters see u-blox documentation UBX-13003221, 32.10.27.1 Navigation/measurement rate settings.

#### Returns

None.

#### Example

```
// Set update frequency to 10 Hz
GPS.setUpdateRate(100, 1, 1);
```

#### See also

* [begin()](#begin)
* [end()](#end)
* [available()](#available)
* [latitude()](#latitude)
* [longitude()](#longitude)
* [speed()](#speed)
* [course()](#course)
* [variation()](#variation)
* [altitude()](#altitude)
* [satellites()](#satellites)
* [getTime()](#gettime)
* [standby()](#standby)
* [setUpdateRate()](#setupdaterate)

