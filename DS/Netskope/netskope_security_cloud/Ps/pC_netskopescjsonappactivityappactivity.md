#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-appactivity
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"nsdeviceuid":""", """"event": """, """"status": """ ]
  Fields = [
    """"status"+:\s+"+({result}[^",]+)""",
# device_classification_status is removed
# user_groups is removed
    """"username"+:\s+"+(({email_address}[^@]+@[^",]+)|({user}[^",]+))""",
# user_source is removed
    """"device_id"+:\s+"+({device_id}F[^",]+)""",
    """"client_version"+:\s+"+({client_version}[^",]+)""",
    """"os"+:\s+"+({os}[^",]+)""",
    """"timestamp"+:\s+({time}\d{10})""",
    """"actor"+:\s+"+(System|User|({user}[^",]+))""",
    """"os_version"+:\s+"+({os_version}[^",]+)""",
# internal_id is removed
    """"device_model"+:\s+"+({device_model}[^",]+)""",
    """"hostname"+:\s+"+({host}[^",]+)""",
# nsdeviceuid is removed
    """"event"+:\s+"+({event_name}[^",]+)""",
# user_key is removed
# npa_status is removed
  ]


}
```