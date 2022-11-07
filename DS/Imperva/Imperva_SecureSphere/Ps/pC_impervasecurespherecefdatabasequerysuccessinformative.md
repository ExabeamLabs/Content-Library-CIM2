#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-query-success-informative
  ParserVersion = v1.0.0
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|SecureSphere|""", """|Audit CounterBreach for Database""", """|Informative|""" ]
  Fields = [
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+)""",
    """\Wsuser=({user}[^\\\s]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsntdom=({domain}[^\s]+)\s+(\w+=|$)""",
    """\Wcat=({db_operation}.+?)\s+(\w+=|$)""",
    """\Wmsg=({db_query}.+?)\s+(\w+=|$)""",
    """\Wdproc=({db_name}.+?)\s+(\w+=|$)""",
    """\Wcn2=({response_size}\d+)\s+(\w+=|$)""",
  ]


}
```