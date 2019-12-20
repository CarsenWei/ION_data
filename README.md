# ION_data
The Urban Data Lab (UDL) provides UBC researchers and operational staff with access to live streaming data on power, energy, water, and gas use of UBC buildings.

## About the Data
Through previous hardware and software investments made by the University, UDL is gaining access to power, energy, water, and gas use data at optimal time and data change intervals. Currently, every building has `energy` and `power` data streams but not all buildings have `gas` and/or `water`. The data is updated with every 2 kW change in the electricity power values but the trigger threshold can be modified in the best interest of researchers and operational staff.

The InfluxDB can be accessed using [command line interface](https://docs.influxdata.com/influxdb/v1.7/tools/shell/) or [client libraries](https://docs.influxdata.com/influxdb/v1.7/tools/api_client_libraries/). The Python notebook `ION influxdb-python Tutorial.ipynb` is a tutorial for accessing and visualizing the data in Python 3.

A Grafana visulization is available [here](https://udl.grafana.net/d/eDDp5YBZk/ion?orgId=1&from=1576705812170&to=1576878612170&panelId=2&fullscreen).
