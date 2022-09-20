#### Parser Content
```Java
{
Name = infowatch-iw-cef-app-login-success-login
  Vendor = InfoWatch
  Product = InfoWatch
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|DLP TM6 Audit|""", """cat=User""", """act=login""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wsuser=({user}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsuid=({full_name}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wad\.user__email=({email_address}[^@]+@({email_domain}.+?))(\s+[\w\.]+=|\s*$)""",
    """"hostname":"({host}[^"]+)"""",
    """"ip":"({dest_ip}[^"]+)"""",
    """"login":"({user}[^"]+)"""",
  ]
  DupFields = [ "host->app" ]


}
```