#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-traffic-dhcpd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""dhcpd""", """bind update on"""]
  Fields = [
    """({event_name}bind update)""",
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+dhcpd(\[\d+\])?: bind update on ({dest_ip}[\da-fA-F.:]+)\s+(got ack\s+)?from\s+({src_host}[^\s:]+):?\s+({additional_info}.+?)\.*"*\s*$""",
  ]


}
```