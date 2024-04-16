#### Parser Content
```Java
{
Name = onapsis-o-json-app-notification-logline
    Vendor=Onapsis
    Product=Onapsis 
    ParserVersion = "v1.0.0"
    ExtractionType = json
    TimeFormat="yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Conditions=[ """"appliances_states":""", """"job_type":""", """"logline":"""  ]
    Fields=[
      """exa_json_path=$.dev_time,exa_field_name=time""",
      # appliance_state is removed
      """exa_json_path=$.event_id,exa_field_name=event_name""",
      # job_type is removed
     ]


}
```