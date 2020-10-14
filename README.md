# ION_data
The Urban Data Lab (UDL) provides UBC researchers and operational staff with access to live streaming data on power, energy, water, and gas use of UBC buildings.

## About the Data
Through previous hardware and software investments made by the University, UDL has gained access to 5-second power, energy, water, and gas use data. In UDL's ION database (Influx database), the data is only updated with **every 2 kW change in the electricity power values** but the trigger threshold can be modified in the best interest of researchers and operational staff.

![database structure](https://github.com/UBC-UrbanDataLab/ION_data/blob/master/images/ION_structure.png)


Currently, every building has `elec_energy` and `elec_power` data streams, but not all buildings have `water_volume` (hot water volume) and/or `gas_volume`. Units of the measurement values: 
- `elec_energy` kWh
- `elec_power` kW
- `water_volume` cubic meter
- `gas_volume` cubic foot, cubic meter, or GJ (refer to the image below). The data in the ION database is **not converted**, so the unit is ft3 if the imae indicates "ft3 => m3".

<p align="center">
  <img width="460" height="300" src="https://github.com/UBC-UrbanDataLab/ION_data/blob/master/images/Gas_unit.png">
</p>


The InfluxDB can be accessed using [command line interface](https://docs.influxdata.com/influxdb/v1.7/tools/shell/) or [client libraries](https://docs.influxdata.com/influxdb/v1.7/tools/api_client_libraries/). The Python notebook `ION influxdb-python Tutorial.ipynb` is a tutorial for accessing and visualizing the data in Python 3.

A Grafana visulization is available [here](https://udl.grafana.net/d/eDDp5YBZk/ion?orgId=1&from=1576705812170&to=1576878612170&panelId=2&fullscreen). Users can click on “Panel Title” and choose “Edit”, which allows them to edit the SQL query and select a time range for the data. 
