## About the Data

The ION database is managed by UBC Energy and Water Services (EWS), which collects data every 5 seconds on electricity (power and energy), hot water, and gas use in campus buildings. In UDL's ION database (Influx database), the data is only updated with **every 2 kW change in the electricity power values** but the trigger threshold can be modified in the best interest of researchers and operational staff.

<p align="center">
  <img width="500" height="350" src="https://github.com/UBC-UrbanDataLab/ION_data/blob/master/images/ION_structure.png">
</p>

Currently, every building has `elec_energy` and `elec_power` data streams, but not all buildings have `water_volume` (hot water volume) and/or `gas_volume`. Units of the measurement values: 
- `elec_energy` kWh
- `elec_power` kW
- `water_volume` cubic meter
- `gas_volume` cubic foot, cubic meter, or GJ (refer to the image below). The data in the ION database is **not converted**, so the unit is ft3 if the image indicates "ft3 => m3".

<p align="center">
  <img width="500" height="400" src="https://github.com/UBC-UrbanDataLab/ION_data/blob/master/images/Gas_unit.png">
</p>

## InfluxDB 2.0 Instance
Public users (read permissions only) can log in to our [**InfluxDB 2.0 User Interface**](http://206.12.92.81:8086/) with the following credentials
- Username:`public02`
- Password: contact UDL (info@urbandatalab.io) to request password

<p align="center">
  <img width="900" src="https://github.com/UBC-UrbanDataLab/ION_data/blob/master/images/ION_UI_Example.JPG">
</p>

Public users can also access this InfluxDB instance from [InfluxDB command line interface](https://docs.influxdata.com/influxdb/v2.0/) or [InfluxDB API client libraries](https://docs.influxdata.com/influxdb/v2.0/tools/client-libraries/) using an authorization token - Please contact UDL (info@urbandatalab.io) to request a token.

[The Python tutorial](https://github.com/UBC-UrbanDataLab/ION_data/blob/master/ION%20InfluxDB%202.0%20Tutorial.ipynb) demonstrates querying the InfluxDB database using the `influxdb-client` Python module. Please [contact UDL](https://urbandatalab.io/) if you have any questions.
