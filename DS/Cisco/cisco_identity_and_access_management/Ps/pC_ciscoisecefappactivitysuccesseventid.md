#### Parser Content
```Java
{
Name = cisco-ise-cef-app-activity-success-eventid
  Vendor = Cisco
  Product = Cisco Identity and Access Management
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [  """|Cisco|Cisco ISE|""", """CEF:""", """msg=""", """eventId=""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """shost=({src_host}[^\s]+)""",
    """Cisco ISE\|(|[^\|]+)\|(|[^\|]+)\|({event_name}[^\|]+)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """dhost=({dest_host}[^\s]+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dpt=({dest_port}\d+)""",
    """Cisco ISE\|*({event_code}\d+)\|""",
    """cat=({category}[^\s]+)\s""",
    """deviceSeverity=({severity}[^\s]+)""",
    """cs1=({auth_method}[^\s]+)""",
  ]


}
```