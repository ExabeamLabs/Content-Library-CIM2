#### Parser Content
```Java
{
Name = infoblox-bddi-json-alert-trigger-success-alert
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "epoch_sec"
  Conditions = [ """"type":"""" ,""""severity":"""",""""message":"""" ,""""subtype":""""]
  Fields = [
    """"id":"({alert_id}[^"]+)"""
    """"type":"({alert_type}[^"]+)"""
    """\ssubtype="({event_name}[^"]+)"""",
    """"account_id":"({account_id}[^"]+)"""
    """"message":"({additional_info}[^"]+?)"""",
    """"severity":"({alert_severity}[^"]+?)"""",
    """Country:\s*({country}[^"<]+)"""
    """City:\s*({city}[^"<]+)"""
    """OS:\s*({os}[^"<]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```