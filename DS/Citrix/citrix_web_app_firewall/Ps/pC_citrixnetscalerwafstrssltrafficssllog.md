#### Parser Content
```Java
{
Name = "citrix-netscalerwaf-str-ssl-traffic-ssllog"
  Vendor = Citrix
  Product = Citrix Web App Firewall
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [
    """-PPE-"""
    """ SSLLOG """
    """SSL_HANDSHAKE"""
  ]
  Fields = [
    """\s+({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)"""
    """\s+({host}[\w\-\.]+)\s+\d+-PPE-\d+\s+:"""
    """-PPE-\d+\s+:(\s+\w+)?\s+({event_name}SSLLOG\s.+?)\s+\d+\s"""
    """\sClientIP\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\sClientPort\s+({src_port}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```