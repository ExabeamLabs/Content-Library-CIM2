#### Parser Content
```Java
{
Name = vmware-horizon-str-endpoint-login-fail-view
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = [ "EEE MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "MMM dd HH:mm:ss"]
  Conditions = [ """ View """, """failed to authenticate because of a bad username or password""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s""",
    """({time}\w{3}\s\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+\d+\s+""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+)\s+({host}[\w\-.]+)\s+View""",
    """User (?:({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  ]
  ParserVersion = "v1.0.0"


}
```