#### Parser Content
```Java
{
Name = kemp-loadbalancer-str-app-activity-l4d
  ParserVersion = "v1.0.0"
  Vendor = Kemp
  Product = Load Balancer
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """l4d: """, """ RS """, """ VS """]
  Fields = [
    """l4d:\s+({event_name}.+?)\s+$""",
    """({event_category}l4d)""",
    """RS\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)\s+to VS\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)\(({dest_host}[^)]+)\)"""
  ]


}
```