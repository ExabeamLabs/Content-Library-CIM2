#### Parser Content
```Java
{
Name = onapsis-o-json-alert-trigger-erphost
    Vendor=Onapsis
    Product=Onapsis
    ParserVersion = "v1.0.0"
    TimeFormat="yyyy-MM-dd'T'HH:mm:ss"
    Conditions=[ """"alarm_name":""", """"erp_host":""", """"incident_detail":""", """"incident_name": "Extraction problem detected in ICM: Extractors Adjusted"""  ]
    Fields=[
      """"created_at":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"username":\s*"({user}[^"]+)""",
      """"incident_name":\s*"({event_name}[^"]+?)\s*"""",no
      """"alarm_name":\s*"({alert_name}[^"]+?)\s*"""",
      """"incident_detail":\s*"({additional_info}[^"]+?)\.?\s*"""",
      """"src":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"source_port":\s*"({src_port}\d+)""",
      """"dst":\s*"(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}[^"]+))"""",
      """"destination_port":\s*"({dest_port}\d+)"""
      """"severity":\s"({alert_severity}[^"]+)"""
]


}
```