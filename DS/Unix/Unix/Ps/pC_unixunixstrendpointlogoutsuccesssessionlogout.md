#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-logout-success-sessionlogout
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """web: web session logout""" ]
  Fields = [
    """web session logout:\s({user}[^\s@]+).+:({src_ip}[\d:.a-fA-F]+)""",
    """\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(\.\S+)?)\S+\s+({host}[^\s]+)\s+({process_name}[^\s]+)\s+({process_id}\d+)\s""",
  ]


}
```