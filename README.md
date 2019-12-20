# ION_data
The Urban Data Lab (UDL) provides access to live streaming data on power, energy, water, and gas use of UBC buildings.

## About the Data
Through previous hardware and software investments made by the University, UDL is gaining access to power, energy, water, and gas use data at optimal time and data change intervals. The data is stored in an InfluxDB instance made accessible to researchers and operational staff at UBC.

The InfluxDB can be accessed using [command line interface](https://docs.influxdata.com/influxdb/v1.7/tools/shell/) or [client libraries](https://docs.influxdata.com/influxdb/v1.7/tools/api_client_libraries/). The Python notebook `ION influxdb-python Tutorial.ipynb` is a tutorial for aceessing and visualizing the data in Python 3.

A Grafana visulization is available [here](https://udl.grafana.net/d/eDDp5YBZk/ion?orgId=1&from=1576705812170&to=1576878612170&panelId=2&fullscreen).
