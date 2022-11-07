#### Parser Content
```Java
{
Name = medigate-m-json-alert-trigger-success-23585
  ParserVersion = v1.0.0
  Vendor = Medigate
  Product = Medigate
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
    """"ip":\s*"({dest_ip}[A-Fa-f\d\.:]+)",\s*"human_name"""",
    """"dest":\s*[^}]+"ip":\s*"({dest_ip}[A-Fa-f\d\.:]+)""",
    """"src_ip":\s*"({src_ip}[A-Fa-f\d\.\:]+)"""",
    """"srcip":\s*"({src_ip}[A-Fa-f\d\.\:]+)"""",
    """"device_category":\s*"({device_category}[^"]+)"""",
    """"device_type_family":\s*"({device_type}[^"]+)"""",
    """"vendor":\s*"({device_vendor}[^"]+)"""",
    """"model":\s*"({device_name}[^"]+)""""
  ]
  DupFields = ["alert-name->alert-type"]


}
```