#### Parser Content
```Java
{
Name = "unix-dhcpd-str-dhcp-session-success-reversemap"
  Vendor = "Unix"
  Product = "Unix dhcpd"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """Added reverse map from """
  ]
  Fields = [
    """\s({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s\w+\["""
    """Added reverse map from (({ip4}\d{1,3})\.({ip3}\d{1,3})\.({ip2}\d{1,3})\.({ip1}\d{1,3})).+? to ({dest_host}[^\s\"$]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```