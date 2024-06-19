# locaspy

locaspy is a Python package designed for retrieving location-based information such as geographical coordinates, weather conditions, ISP details, and more, using an IP address as input.

## Benefits

- ***Convenience*** : Easily retrieve detailed information about any IP address.
- ***Flexibility*** : Retrieve specific details such as weather, location, ISP, and more.
- ***Integration*** : Useful for integration into applications needing location-based services.
- ***Accuracy*** : Utilizes reliable APIs to provide accurate information.

## Who Would Benefit?

- ***Developers*** : Integrate location-based features into applications.
- ***Network Administrators*** : Quickly gather IP-related details.
- ***Security Analysts*** : Obtain context about IP addresses during investigations.

## Installation

You can install locaspy via pip:

```bash
pip install locaspy
```

## Usage
### Overview

- locaspy provides functions to fetch various types of information based on an IP address.

<b>How do you print your IP address?</b>
```python
import locaspy

my_ip = locaspy.get_my_ip()
print("My IP Address:", my_ip)
```
<b>Here's how you can use the locaspy package to print all available information based on the user's IP address:</b>
```python
import locaspy

# Get the user's IP address
ip_address = locaspy.get_ip()

# Get all information based on the IP address
info = locaspy.get_data(ip_address)

# Print all information
print("IP Address:", info["ip_address"])
print("Google Maps Link:", info["map_link"])
print("Location:")
print(f"  City: {info['city']}")
print(f"  Region: {info['region']}")
print(f"  Country: {info['country']}")
print(f"  Latitude: {info['latitude']}")
print(f"  Longitude: {info['longitude']}")
print(f"  Timezone: {info['timezone']}")
print(f"  Country Code: {info['country_code']}")
print(f"  Country Capital: {info['country_capital']}")
print(f"  ISP: {info['isp']}")
print(f"  ASN: {info['asn']}")
print(f"  Organization: {info['organization']}")
print(f"  Postal Code: {info['postal']}")
print(f"  UTC Offset: {info['utc_offset']}")
print(f"  Continent: {info['continent']}")
print(f"  Currency: {info['currency']}")
print(f"  Languages: {info['languages']}")
print("Weather:")
print(f"  Condition: {info['weather_condition']}")
print(f"  Temperature: {info['temperature']}°C")
print(f"  Wind Speed: {info['wind_speed']} km/h")
```

### Example Usages

<b>Get Google Maps Link</b>
```python
import locaspy

ip_address = input("Enter your IP: ")
map_link = locaspy.get_data(ip_address, "map")
print("Google Maps Link:", map_link)
```

<b>Get Weather Information</b>

```python
import locaspy

ip_address = input("Enter your IP: ")
weather_info = locaspy.get_data(ip_address, "weather")
print("Weather Information:", weather_info)
```

<b>Get Location Details</b>
```python
import locaspy

ip_address = input("Enter your IP: ")
location_info = locaspy.get_data(ip_address, "location")
print("Location Details:\n", location_info)
```

<b>Get ISP Information</b>
```python
import locaspy

ip_address = input("Enter your IP: ")
isp_info = locaspy.get_data(ip_address, "isp")
print("ISP Information:", isp_info)
```

<b>Get ASN Information</b>
```python
import locaspy

ip_address = input("Enter your IP: ")
asn_info = locaspy.get_data(ip_address, "asn")
print("ASN Information:", asn_info)
```

<b>Get Postal Code</b>
```python
import locaspy

ip_address = input("Enter your IP: ")
postal_code = locaspy.get_data(ip_address, "postal")
print("Postal Code:", postal_code)
```

<b>Get Continent</b>
```python
import locaspy

ip_address = input("Enter your IP: ")
continent = locaspy.get_data(ip_address, "continent")
print("Continent:", continent)
```

<b>Get Currency<b>
```python
import locaspy

ip_address = input("Enter your IP: ")
currency = locaspy.get_data(ip_address, "currency")
print("Currency:", currency)
```

<b>Get Languages</b>
```python
import locaspy

ip_address = input("Enter your IP: ")
languages = locaspy.get_data(ip_address, "languages")
print("Languages:", languages)
```

<b>To save all data in a single file</b>
```python
import locaspy

# Get the user's IP address
ip_address = locaspy.get_ip()

# Get all information based on the IP address
info = locaspy.get_data(ip_address)

# Define the file path
file_path = "data.txt"

# Open the file in write mode and write the information
with open(file_path, "w") as file:
    file.write(f"IP Address: {info['ip_address']}\n")
    file.write(f"Google Maps Link: {info['map_link']}\n")
    file.write("Location:\n")
    file.write(f"  City: {info['city']}\n")
    file.write(f"  Region: {info['region']}\n")
    file.write(f"  Country: {info['country']}\n")
    file.write(f"  Latitude: {info['latitude']}\n")
    file.write(f"  Longitude: {info['longitude']}\n")
    file.write(f"  Timezone: {info['timezone']}\n")
    file.write(f"  Country Code: {info['country_code']}\n")
    file.write(f"  Country Capital: {info['country_capital']}\n")
    file.write(f"  ISP: {info['isp']}\n")
    file.write(f"  ASN: {info['asn']}\n")
    file.write(f"  Organization: {info['organization']}\n")
    file.write(f"  Postal Code: {info['postal']}\n")
    file.write(f"  UTC Offset: {info['utc_offset']}\n")
    file.write(f"  Continent: {info['continent']}\n")
    file.write(f"  Currency: {info['currency']}\n")
    file.write(f"  Languages: {info['languages']}\n")
    file.write("Weather:\n")
    file.write(f"  Condition: {info['weather_condition']}\n")
    file.write(f"  Temperature: {info['temperature']}°C\n")
    file.write(f"  Wind Speed: {info['wind_speed']} km/h\n")

# Print confirmation message
print(f"Data has been saved to {file_path}")
```

## Thanks

Thank you for using locaspy! We appreciate your interest in our tool and hope it meets your needs. 

## Additional Information

For any issues, suggestions, or contributions, please visit our [GitHub repository](https://github.com/ByteBreach/locaspy) 

We welcome and encourage contributions from the community. Whether it's reporting a bug, suggesting a feature, or improving the documentation, your feedback is valuable and helps us improve the project.

### License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/ByteBreach/locaspy/LICENSE) file for details.

### Acknowledgements

We would like to acknowledge the following libraries and resources that made this project possible:
- [requests](https://pypi.org/project/requests/)
- [ipapi](https://ipapi.co/)
- [open-meteo](https://open-meteo.com/)

Thank you again for your support!
