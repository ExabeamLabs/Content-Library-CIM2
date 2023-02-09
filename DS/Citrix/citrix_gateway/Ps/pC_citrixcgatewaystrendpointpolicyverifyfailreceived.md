#### Parser Content
```Java
{
Name = citrix-cgateway-str-endpoint-policy-verify-fail-received
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """ AAA Message """, """No valid RADIUS responses received""" ]
  Fields = [
    """({time}\d+\/\d+\/\d+:\d+:\d+:\d+)\s*GMT""",
    """GMT\s*({host}[^:\s]+)(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*"*({additional_info}[^"]+)"*"""
  ]
  DupFields = ["host->src_host"]


}
```