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
    """\Wsuser=({user}[\w\.\-]{1,40}\$?)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsntdom=({domain}[^\s]+)\s+(\w+=|$)""",
    """\Wcat=({db_operation}.+?)\s+(\w+=|$)""",
    """\Wmsg=({db_query}.+?)\s+(\w+=|$)""",
    """\Wdproc=({db_name}.+?)\s+(\w+=|$)""",
    """\Wcn2=({response_size}\d+)\s+(\w+=|$)""",
  ]


}
```