# Evolution Lab - Netbox using Pynetbox and Napalm

Following the instructions below:


# Dependencies:

Install the requirements to install all dependencies:

$ pip install -r requirements.txt


# Endpoint

NETBOX_URL = "https://demo.netbox.dev/"
If necessary, change that for another one, all my codes was tested in "https://netbox.int.flexcloud.com.br/"


# Authentication:

Put api token, URL, username and password informations into variables in config.py file.

api_key = ""
nb_username = ""
nb_password = ""
nb_url = ""


# IP/FQDN

I used WSL (Windows Subsystem Linux) to tests all codes, so access by SSH was done with FQDN, all devices needed in /etc/hosts, because I searching for model in device_type to take the hostname of devices.

e.g: 
nxos_model = list(nb.dcim.devices.filter(model="nexus-9300"))

# Exercises:

4 - Collect information for devices with Status = Active, Tenant = NOC in Netbox Doing a loop to find Status = Active, Tenant = NOC in Netbox
  Using file collect_status.py

5 - Information to collect: software version Custom field to update: "sw_version" Assume network device list would contain Cisco Catalyst IOS
  Using files update_nxos_custfields.py, update_ios_custfields.py and update_iosxr_custfields.py


# Note:

I need more concepts about class and functions to create pytest file to works properly. So the files start with test_* name doesn't work from pytest.
