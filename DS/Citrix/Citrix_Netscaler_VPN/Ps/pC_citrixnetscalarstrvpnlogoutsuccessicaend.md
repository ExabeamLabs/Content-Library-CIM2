#### Parser Content
```Java
{
Name = citrix-netscalar-str-vpn-logout-success-icaend
    ParserVersion = v1.0.0
    Vendor = Citrix
    Product = Citrix Netscaler VPN
    TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
    Conditions = [ """ SSLVPN ICAEND_CONNSTAT """ ]
    Fields = [
    """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+SSLVPN ({event_name}ICAEND_CONNSTAT)\s""",
    """\sSource\s+({src_ip}[a-fA-F\d.:]+?)(:({src_port}\d+))?\s""",
    """\sDestination\s+({dest_ip}[a-fA-F\d.:]+?)(:({dest_port}\d+))?\s""",
    """\susername:domainname\s+({user}[^\s:]+):({domain}[^\s]+)""",
    """\sDuration ({duration}\S+)""",
    """\sTotal_bytes_send\s+({bytes_out}\d+)""",
    """\sTotal_bytes_recv\s+({bytes_in}\d+)""",
    """\sconnectionId\s+({source_connection_id}\S+?)($|")"""
  ]


}
```