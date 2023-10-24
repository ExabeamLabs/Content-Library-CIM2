#### Parser Content
```Java
{
Name = unix-unix-sk4-endpoint-logout-success-connectionclosed
  ParserVersion = v1.0.0
  Product = Unix
  Vendor = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"ident":"sshd""", """Connection closed""" ]
  Fields = [
    """"host":"({host}[^"]+)""",
    """"timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""
    """"ident":"({event_code}[^"]+)""",
    """"pid":"({process_id}\d+)""",
    """Connection closed by ({src_ip}[A-Fa-f.:\d]+)\s+port\s+({src_port}\d+)""",
    """({event_name}Connection closed)"""
  ]


}
```