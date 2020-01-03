## Laravel Unit Conversion

This package helps to convert units. It was forked from [abhimanyu003/conversion](https://github.com/abhimanyu003/conversion) repository.

### Units supported

-   Acceleration
-   Angle
-   Area
-   Storage
-   Current
-   Fuel
-   Length
-   Mass
-   Pressure
-   Speed
-   Temperature
-   Time
-   Voltage
-   Volume

### Installation

```php
composer require becker/conversion
```

### Register the Service Provider

> **NOTE:** You can skip this step if you are using Laravel 5.5 or higher. The package is automatically registered, due to the [package discovery](https://laravel.com/docs/master/packages#package-discovery) feature.

Open up the `config/app.php` and register the new Service Provider:

```php
//config/app.php

/*
 * Package Service Providers...
 */

Becker\Conversion\ConversionServiceProvider::class

//...
```

You can also register the Alias:

```php
'Conversion'  => Becker\Conversion\Facades\Conversion::class
```

### How to use

```php
Conversion::convert($value, 'type')->to('another_type');
```

#### Example:

-   Converting MB to KB

```php
Conversion::convert(1, 'megabyte')->to('kilobyte');
// 1.024,00 (two decimal places)
```

-   Converting mm to cm

```php
Conversion::convert(1000, 'millimeter')->to('centimeter');
```

-   Converting kg to g

```php
Conversion::convert(1, 'kilogram')->to('gram');
```

### Formatting results:

```php
Conversion::convert($value, 'type')->to('another_type')
->format(int decimal, 'decimal place modifier', 'thousand place modifier');
```

#### Example:

```php
Conversion::convert(1, 'megabyte')->to('kilobyte')->format(0,'.',',');
// 1,024 (no decimal place)
```

### Conversion Chart

#### Acceleration

-   METRE_PER_SECOND_SQUARE

#### Angle

-   TURN
-   RADIAN
-   DEGREE
-   GRADIAN

#### Area

-   SQUARE_METER
-   HECTARE
-   SQUARE_KILOMETER
-   SQUARE_INCH
-   SQUARE_FEET
-   SQUARE_YARD
-   ACRE
-   SQUARE_MILE

#### Storage

-   BIT
-   BYTE
-   KILOBIT
-   KILOBYTE
-   MEGABIT
-   MEGABYTE
-   GIGABIT
-   GIGABYTE
-   TERABIT
-   TERABYTE
-   PETABIT
-   PETABYTE

#### Current

-   STATAMPERE
-   MICROAMPERE
-   MILLIAMPERE
-   AMPERE
-   ABAMPERE
-   KILOAMPERE

#### Fuel

-   KILOMETERS_PER_LITRE
-   LITRE_PER_100_KILOMETER
-   MILES_PER_GALLON
-   US_MILES_PER_GALLON

#### Length

-   MILLIMETER
-   CENTIMETER
-   METER
-   KILOMETER
-   INCH
-   FOOT
-   YARD
-   MILE
-   NAUTICAL_MILE

#### Mass

-   MICROGRAM
-   MILLIGRAM
-   GRAM
-   KILOGRAM
-   METRIC_TON
-   OUNCE
-   POUND
-   STONE
-   SHORT_TON
-   LONG_TON

#### Pressure

-   PASCAL
-   KILOPASCAL
-   MEGAPASCAL
-   BAR
-   MILLIMETERS_OF_MERCURY
-   INCHES_OF_MERCURY
-   POUNDS_PER_SQUARE_INCH
-   ATMOSPHERE

#### Speed

-   METER_PER_SECOND
-   KILOMETERS_PER_HOUR
-   FEET_PER_SECOND
-   MILES_PER_HOUR
-   KNOT

#### Temperature

-   CELSIUS
-   FAHRENHEIT
-   KELVIN

#### Time

-   NANOSECOND
-   MICROSECOND
-   MILLISECOND
-   SECOND
-   MINUTE
-   HOUR
-   DAY
-   WEEK
-   MONTH
-   YEAR
-   DECADE
-   CENTURY
-   MILLENIUM

#### Voltage

-   VOLT
-   KILOVOLT

#### Volume

-   MILLILITRE
-   LITRE
-   CUBIC_METER
-   GALLON
-   QUART
-   PINT
-   TABLESPOON
-   TEASPOON
-   US_GALLON
-   US_QUART
-   US_PINT
-   US_CUP
-   US_OUNCE
-   US_TABLESPOON
-   US_TEASPOON
-   CUBIC_INCH
-   CUBIC_FOOT

### Contribute

Feel free to contribute and update the repository.
