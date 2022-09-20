#### Parser Content
```Java
{
Name = medigate-m-json-alert-trigger-success-iot
  ParserVersion = v1.0.0
  Vendor = Medigate
  Product = Medigate
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"device_category": "IoT"""", """"event_type":""", """"device_type_family":""" ]
  Fields = [
    """\d\d:\d\d:\d\d[\d\.\+:\-]+\s+({host}[\w\-\.]+)\s*""",
    """"insertion_time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\+[\d\:]+)"""",
    """"event_type":\s*"({alert_name}[^"]+)"""",
    """"severity":\s*"({alert_severity}[^"]+)"""",
    """"text":\s*"({additional_info}[^"]+)"""",
    """"protocol":\s*"({protocol}[^"]+)"""",
    """"dest":\s*[^\}]+"ip":\s*"({dest_ip}[A-Fa-f\d\.:]+)""",
    """"ip":\s*"({src_ip}[A-Fa-f\d\.:]+)"""",
    """"device_category":\s*"({device_category}[^"]+)"""",
    """"device_type_family":\s*"({device_type}[^"]+)"""",
    """"vendor":\s*"({device_vendor}[^"]+)"""",
    """"model":\s*"({device_name}[^"]+)""""
  ]
  DupFields = ["alert_name->alert_type"]


}
```