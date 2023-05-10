#### Parser Content
```Java
{
Name = citrix-cgateway-str-network-close-tcpconn
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """-PPE-""", """ TCP """, """CONN_""" ]
  Fields = [
    """\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+\S+\s+\d+-PPE-\d+\s*:""",
    """End Time\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)""",
    """Delink Time\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)""",
    """({host}[^\s]+)\s+\d+-PPE-\d+\s+:""",
    """-PPE-\d+\s+:(\s+\w+)?\s+({event_name}TCP\s.+?)\s+\d+\s""",
    """\sSource\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+)""",
    """\sDestination\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)""",
    # DL Fields are removed
    """\sNatIP\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_translated_port}\d+)""",
    """Total_bytes_send ({bytes_out}\d+)""",
    """Total_bytes_recv ({bytes_in}\d+)""",
  ]


}
```