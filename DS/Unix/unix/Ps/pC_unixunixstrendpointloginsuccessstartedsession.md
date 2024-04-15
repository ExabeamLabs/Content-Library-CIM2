#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-success-startedsession"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """systemd: Started Session"""
  ]
  Fields = [
    """({host}[\w\-.]+)\s+systemd: Started Session"""
    """of user ({user}[^\s\.]+)"""
    """({event_code}Started Session)"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```