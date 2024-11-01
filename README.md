# POC_dkwe70

## Getting started


**Create a Custom Credential for Cisco ACI** <br>
Input Configuration:
```
fields:
  - id: aci_host
    type: string
    label: Host
  - id: aci_username
    type: string
    label: Username
  - id: aci_password
    type: string
    label: Password
    secret: true
required:
  - host
  - username
  - password
```
Injector Configuration
```
extra_vars:
  host: '{{ aci_host }}'
  password: '{{ aci_password }}'
  username: '{{ aci_username }}'
```

**Create a Custom Credential for NetApp_OnTap** <br>
Input Configuration:
```
fields:
  - id: netapp_instance
    type: string
    label: Netapp_Instance
  - id: netapp_username
    type: string
    label: Username
  - id: netapp_password
    type: string
    label: Password
    secret: true
required:
  - netapp_instance
  - netapp_username
  - netapp_password

```
Injector Configuration
```
extra_vars:
  netapp_instance: '{{ netapp_instance }}'
  netapp_password: '{{ netapp_password }}'
  netapp_username: '{{ netapp_username }}'
```
**Other Credentials** <br>
F5 requires the Network credential type <br>
Linux and Windows require the Machine credential type