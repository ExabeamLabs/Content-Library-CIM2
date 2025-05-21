#### Parser Content
```Java
{
Name = mcafee-mdam-cef-alert-trigger-success-alert-1
  Vendor = Trellix
  Product = Trellix Database Security
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|McAfee|Database Security|""", """|alert|"""]
  Fields = [
    """Exec_Time=\\"({time}\d\d\s\w\w\w\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """({host}[\w\-\.]+)\s*CEF:""",
    """\|alert\|({alert_name}[^\|]+)""",
    """Src_Host=\\"(\.|({src_host}[\w\-\.]+))""",
    """Src_IP=\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Severity=\\"({alert_severity}[^"\\]+)""",
    """DB_Name =\\"({db_name}[^"]+)\\"""",
    """\sExec_User=\\"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """OS_User=\\"([^\\]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Statement=\\"({db_query}({db_operation}\w+)[^$]+)\s*\\?$"""
  ]
  ParserVersion = v1.0.0


}
```