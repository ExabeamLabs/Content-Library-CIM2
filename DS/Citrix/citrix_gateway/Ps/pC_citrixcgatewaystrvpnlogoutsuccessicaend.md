#### Parser Content
```Java
{
Name = citrix-cgateway-str-vpn-logout-success-icaend
    ParserVersion = v1.0.0
    Vendor = Citrix
    Product = Citrix Gateway
    TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
    Conditions = [ """ SSLVPN ICAEND_CONNSTAT """ ]
    Fields = [
    """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+SSLVPN ({event_name}ICAEND_CONNSTAT)\s""",
    """\sSource\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """\sDestination\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
    """\susername:domainname\s+({user}[^\s:]+):({domain}[^\s]+)""",
    """\sDuration ({duration}\S+)""",
    """\sTotal_bytes_send\s+({bytes_out}\d+)""",
    """\sTotal_bytes_recv\s+({bytes_in}\d+)""",
    """\sconnectionId\s+({source_connection_id}\w+)\s"""
    """\sconnectionId\s+({source_connection_id}\S+?)($|")"""
  ]


}
```