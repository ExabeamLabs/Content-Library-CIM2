#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-activity-sudo"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """sudo:"""
    """ PAM """ 
  ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+)? sudo:"""
    """\ssudo:\s*({additional_info}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```