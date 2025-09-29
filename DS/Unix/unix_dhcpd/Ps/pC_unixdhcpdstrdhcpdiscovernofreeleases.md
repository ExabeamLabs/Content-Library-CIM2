#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-discover-nofreeleases
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """dhcpd""", """DHCPDISCOVER from""", """ no free leases""" ]
  Fields = [
    """\s({host}[^\s]+)\s+dhcpd""",
    """dhcpd\[({service_id}\d+)\]""",
    """dhcpd\[\d+\]:\s+({event_name}.+\S)""",
    """dhcpd\[\d+\]:\s+({event_name}DHCPDISCOVER)""",
    """\d\d:\d\d:\d\d\s\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}\s({app}[^\[]+)\[""",
    """ from (({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({dest_mac}\S\S:\S\S:\S\S:\S\S:\S\S:\S\S)) """,
    """via ({dest_interface}[^\s"]+)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```