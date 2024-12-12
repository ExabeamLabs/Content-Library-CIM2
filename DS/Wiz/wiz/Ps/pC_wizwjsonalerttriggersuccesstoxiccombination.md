#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-toxiccombination
  Vendor = Wiz
  Product = Wiz
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  Conditions = [ """"type":"TOXIC_COMBINATION"""", """"entitySnapshot":""", """"control":{""" ]
  Fields = [
    """"createdAt":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"control"[^\}]+?"name":"({alert_name}[^"]+)"""",
    """"control"[^\}]+?"id":"({alert_id}[^"]+)"""",
    """({alert_type}TOXIC_COMBINATION)""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"control"[^\}]+?"description":"({alert_description}[^"]+)"""",
    """"status":"({alert_status}[^"]+)"""",
    """"entitySnapshot"[^\}]+?"type":"({resource_type}[^"]+)"""",
    """"entitySnapshot"[^\}]+?"name":"({resource_name}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```