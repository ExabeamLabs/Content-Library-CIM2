#### Parser Content
```Java
{
Name = skyformation-s-sk4-app-login-login
  ParserVersion = "v1.0.0"
  Vendor = Skyformation
  Product = Skyformation
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =""", """suser=""", """"Action":"Login"""" ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)""",
    """\Wend=({time}\d+)""",
    """\Wdproc=({process_name}.+?)(\s+\w+=|\s*$)""",
    """\Wfname=(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wmsg=({additional_info}.+?)(\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))""",
    """\Wsuser=({full_name}\w+(\s+\w+)+)""",
  ]


}
```