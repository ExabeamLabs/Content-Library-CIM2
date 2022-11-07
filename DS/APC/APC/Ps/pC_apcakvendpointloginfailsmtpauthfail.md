#### Parser Content
```Java
{
Name = apc-a-kv-endpoint-login-fail-smtpauthfail
  ParserVersion = v1.0.0
  Vendor = APC
  Product = APC
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss.SSS"
  Conditions = [ """type=statistics """, """classifier="SMTP Auth Failure"""", """disposition="Reject"""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d\stime=\d\d:\d\d:\d\d\.\d{1,3})""",
    """client_name="({src_host}[^"]+?)\s*"""",
    """client_ip="({src_ip}[a-fA-F\d:\.]+)"""",
    """dst_ip="({dest_ip}[a-fA-F\d:\.]+)"""",
    """from="({user}[^"]+)"""",
    """classifier="({event_name}[^"]+)"""",
    """disposition="({action}[^"]+)""""
  ]
  DupFields = [ "event_name->failure_reason" ]


}
```