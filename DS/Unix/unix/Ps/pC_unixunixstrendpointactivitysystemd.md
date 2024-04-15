#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-activity-systemd"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """systemd["""
    """]: """
  ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}\S+)? systemd\["""
    """\ssystemd(-logind)?\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```