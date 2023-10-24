#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-activity-kernel"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """ kernel: hub """ 
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?\s*({host}[^\s]+)\s*kernel:"""
    """\skernel:\s*({additional_info}.+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```