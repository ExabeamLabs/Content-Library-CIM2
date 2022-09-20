#### Parser Content
```Java
{
Name = unix-dhcpd-str-app-notification-reuselease
    ParserVersion = v1.0.0
    Vendor = Unix
    Product = Unix dhcpd
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ dhcpd: reuse_lease: """ ]
    Fields = [
      """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w.\-]+) dhcpd:\s+({event_name}reuse_lease):\s+lease age (\d+)""", #dl field removed
      """lease for ({dest_ip}[a-fA-F\d.:]+)""",
    ]
  

}
```