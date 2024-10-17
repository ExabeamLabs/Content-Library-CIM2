#### Parser Content
```Java
{
Name = cisco-c-mix-endpoint-logout-success-sessionexited
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = ["MMM dd yyyy HH:mm:ss a","MMM dd yyyy HH:mm:ss.SSS", "MMM dd HH:mm:ss.SSS"]
  ParserVersion = "v1.0.0"
  Conditions = [ """-LOGOUT: """, """has exited tty session""" ]
  Fields = [
    """\s({time}\w{3}\s\d{2}\s\d{0,4}\s*\d\d:\d\d:\d\d\.\d+)\s\w+""",
    """<\d+>[^:\s]+:\s+({host}[^:\s]+):""",
    """({event_code}\S+\d+-LOGOUT):""",
    """User\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+has exited tty session""",
    """\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?)\)\s*$""",
  ] 


}
```