#### Parser Content
```Java
{
Name = logbinder-sqlserver-cef-database-activity-logbindersql
  Vendor = LOGBinder
  Product = LOGBinder for SQL Server
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss z"
  Conditions = [ """CEF:""", """|LOGbinder|SQL|""" ]
  Fields = [
    """({host}[\w.\-]+)\s+CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({event_name}[^\|]+)""",
    """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)""",
    """\W(d|s)user=(n/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\WdeviceExternalId=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """<address>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</address>""",
    """\Wcs6=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
  ]


}
```