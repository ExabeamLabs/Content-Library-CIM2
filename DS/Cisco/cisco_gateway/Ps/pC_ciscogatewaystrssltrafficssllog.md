#### Parser Content
```Java
{
Name = "cisco-gateway-str-ssl-traffic-ssllog"
  Vendor = "Cisco"
  Product = "Cisco Gateway"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [
    """-PPE-"""
    """ SSLLOG """
    """SSL_"""
  ]
  Fields = [
    """\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+\S+\s+\d+-PPE-\d+\s*:"""
    """({host}[^\s]+)\s+\d+-PPE-\d+\s+:"""
    """-PPE-\d+\s+:(\s+\w+)?\s+({event_name}SSLLOG\s.+?)\s+\d+\s"""
    """\sClientIP\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\sClientPort\s+({src_port}\d+)"""
# vserver_ip is removed
# vserver_port is removed
# session is removed
  ]
  ParserVersion = "v1.0.0"


}
```