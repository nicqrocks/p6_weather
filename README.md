#Goal

Give basic info on the current weather for a given location provided through a module. The module should be able to change services very easily incase something happens to one of them.
Information given will include:
- temperature
- possibility of precipitation
- wind speed

This info will only be provided for the current day.

##Interface

###`weather-for`

    my $result = weather-for 'Detroit', 'us';
    printf "Current weather is: %d℃, %dmm precip/3hr, wind %dm/s\n",
        .temp, .precip, .wind given $result;

The function will take two positional arguments: name of the city and [ISO country code](http://www.nationsonline.org/oneworld/country_code_list.htm). The country is optional and by default is not specified. A `Weather::Result` object will be returned on success, otherwise it will give a `Failure`.

###`.temp`

    say "Current temperature is: $result.temp()℃";

This function takes no arguments and will return a `Numeric` amount in degrees celsius.

###`.precip`

    say "Expected to receive $result.precip()mm/3hr of precipitation";

This function takes no arguments and will return a `Numeric` amount of precipitation in millimeters per three hours.

###`.wind`

    say "Wind speed is: $result.wind()m/s";

This function takes no arguments and returns a `Numeric` speed in meters per second.



####Source
This project is from a walkthrough found at [perl6.party](http://perl6.party/post/Perl-6-Hands-On-Workshop--Weatherapp--Part-1)
