#### Parser Content
```Java
{
Name = onapsis-o-json-app-notification-logline
    Vendor=Onapsis
    Product=Onapsis 
    ParserVersion = "v1.0.0"
    TimeFormat="yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Conditions=[ """"appliances_states":""", """"job_type":""", """"logline":"""  ]
    Fields=[
      """"dev_time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)""",
# appliance_state is removed
      """"event_id":\s*"({event_name}[^"]+)""",
# job_type is removed
     ]


}
```