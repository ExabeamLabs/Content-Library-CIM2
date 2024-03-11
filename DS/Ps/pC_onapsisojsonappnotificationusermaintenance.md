#### Parser Content
```Java
{
Name = onapsis-o-json-app-notification-usermaintenance
    Vendor=Onapsis
    Product=Onapsis
    ParserVersion = "v1.0.0"
    TimeFormat="yyyy-MM-dd'T'HH:mm:ss"
    Conditions=[ """"alarm_name":""", """"erp_host":""", """"incident_detail":""", """"incident_name": "User Maintenance"""  ]
    Fields=[
      """"created_at":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"username":\s*"({user}[^"]+)""",
      """"incident_name":\s*"({event_name}[^"]+?)\s*"""",
      """"alarm_name":\s*"({alert_name}[^"]+?)\s*"""",
      """"incident_detail":\s*"({additional_info}[^"]+?)\.?\s*"""",
      """"src":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"source_port":\s*"({src_port}\d+)""",
      """"dst":\s*"(({dest_host}[^"]+)|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
      """"destination_port":\s*"({dest_port}\d+)"""
]


}
```