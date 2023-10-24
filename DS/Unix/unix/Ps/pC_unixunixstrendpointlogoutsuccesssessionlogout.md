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
    """web session logout:\s({user}[\w\.\-]{1,40}\$?).+:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(\.\S+)?)\S+\s+({host}[^\s]+)\s+({process_name}[^\s]+)\s+({process_id}\d+)\s""",
  ]


}
```