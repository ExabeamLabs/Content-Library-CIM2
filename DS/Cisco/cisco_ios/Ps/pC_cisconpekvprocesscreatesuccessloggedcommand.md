#### Parser Content
```Java
{
Name = cisco-npe-kv-process-create-success-loggedcommand
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss.SSS"]
  Conditions = [ """CFGLOG_LOGGEDCMD:""", """logged command:""" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d\.\d+)""",
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """(\w{3}\s(\d\d|\s\d)\s(\d\d\d\d\s)?(\d\d| \d):\d\d:\d\d)\s+({host}[\w.\-:]+?[^:])\s*:?\s*%ASA-""",
    """User:\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
    """logged command:[\s\*]*({process_command_line}({process_name}[^\s]+)?.+?)?[\s\*]*(Source:\s*\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|$)""",
    """Original Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]


}
```