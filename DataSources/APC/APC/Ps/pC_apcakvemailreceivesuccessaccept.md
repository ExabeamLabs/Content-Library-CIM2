#### Parser Content
```Java
{
Name = apc-a-kv-email-receive-success-accept
  ParserVersion = v1.0.0
  Vendor = APC
  Product = APC
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss.SSS"
  Conditions = [ """type=statistics """, """classifier="Access Control-Safe-Relay"""", """disposition="Accept"""", """direction="in"""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d\stime=\d\d:\d\d:\d\d\.\d{1,3})""",
    """pri=({alert_severity}[^\s]+)""",
    """client_name="({src_host}[^"]+)"""",
    """client_ip="({src_ip}[a-fA-F\d:\.]+)"""",
    """dst_ip="({dest_ip}[a-fA-F\d:\.]+)"""",
    """from="({email_address}[^"]+)"""",
    """to="({dest_email_address}[^"]+)"""",
    """domain="({domain}[^"]+)"""",
    """direction="({direction}[^"]+)"""",
    """classifier="({alert_name}[^"]+)"""",
    """disposition="({action}[^"]+)"""",
    """subject="({email_subject}[^"]+)""""
  ]


}
```