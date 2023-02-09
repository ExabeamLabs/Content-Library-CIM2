#### Parser Content
```Java
{
Name = unix-unix-sk4-endpoint-logout-success-disconnectedbyuser
  Product = Unix
  Vendor = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"ident":"sshd""", """Received disconnect""", """disconnected by user""" ]
  Fields = [
    """"host":"({host}[^"]+)""",
    """"timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
    """"ident":"({event_code}[^"]+)""",
    """"pid":"({process_id}\d+)""",
    """Received disconnect from\s+({src_ip}[A-Fa-f.:\d]+)\s+port\s+({src_port}\d+)""",
    """({event_name}disconnected by user)"""
  ]


}
```