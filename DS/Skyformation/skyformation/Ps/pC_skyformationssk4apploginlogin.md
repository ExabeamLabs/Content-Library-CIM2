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
    """\Wend=({time}\d{13})""",
    """\Wdproc=({process_name}.+?)(\s+\w+=|\s*$)""",
    """\Wfname=(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wmsg=({additional_info}.+?)(\s+\w+=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))""",
    """\Wsuser=({full_name}\w+(\s+\w+)+)""",
  ]


}
```