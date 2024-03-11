#### Parser Content
```Java
{
Name = claroty-c-json-alert-trigger-success-23585
  ParserVersion = v1.0.0
  Vendor = Claroty
  Product = Claroty
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"device_category":""", """"event_type":""", """"device_type_family":""" ]
  Fields = [
    """\d\d:\d\d:\d\d[\d\.\+:\-]+\s+({host}[\w\-\.]+)\s*""",
    """"insertion_time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\+[\d\:]+)"""",
    """"event_type":\s*"({alert_name}[^"]+)"""",
    """"severity":\s*"({alert_severity}[^"]+)"""",
    """"text":\s*"({additional_info}[^"]+)"""",
    """"protocol":\s*"({protocol}[^"]+)"""",
    """"ip_proto":\s*({protocol}\d+)""",
    """"ip":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?",\s*"human_name"""",
    """"dest":\s*[^}]+"ip":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"src_ip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"srcip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"device_category":\s*"({device_category}[^"]+)"""",
    """"device_type_family":\s*"({device_type}[^"]+)"""",
    """"vendor":\s*"({device_vendor}[^"]+)"""",
    """"model":\s*"({device_name}[^"]+)""""
  ]
  DupFields = ["alert-name->alert-type"]


}
```