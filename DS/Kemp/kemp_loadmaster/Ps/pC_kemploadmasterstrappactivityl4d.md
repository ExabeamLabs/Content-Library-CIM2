#### Parser Content
```Java
{
Name = kemp-loadmaster-str-app-activity-l4d
  ParserVersion = "v1.0.0"
  Vendor = Kemp
  Product = Kemp LoadMaster
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """l4d: """, """ RS """, """ VS """]
  Fields = [
    """l4d:\s+({event_name}.+?)\s+$""",
    """({event_category}l4d)""",
    """RS\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\s+to VS\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)\(({dest_host}[^)]+)\)"""
  ]


}
```