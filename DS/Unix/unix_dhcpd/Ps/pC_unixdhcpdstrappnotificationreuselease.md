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
      """lease for ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    ]
  

}
```