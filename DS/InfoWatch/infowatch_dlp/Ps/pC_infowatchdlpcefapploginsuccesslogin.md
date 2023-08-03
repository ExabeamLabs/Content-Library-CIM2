#### Parser Content
```Java
{
Name = infowatch-dlp-cef-app-login-success-login
  Vendor = InfoWatch
  Product = InfoWatch DLP
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|DLP TM6 Audit|""", """cat=User""", """act=login""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsuser=({user}[\w\.\-]{1,40}\$?)(\s+[\w\.]+=|\s*$)""",
    """\Wsuid=({full_name}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wad\.user__email=({email_address}[^@]+@({email_domain}.+?))(\s+[\w\.]+=|\s*$)""",
    """"hostname":"({host}[^"]+)"""",
    """"ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"login":"({user}[\w\.\-]{1,40}\$?)"""",
  ]
  DupFields = [ "host->app" ]


}
```