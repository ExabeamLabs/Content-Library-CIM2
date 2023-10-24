#### Parser Content
```Java
{
Name = microsoft-mssql-kv-app-login-fail-18456
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=18456""", """Keywords=Audit Failure""", """Login failed""" ]
  Fields = [
    """(\\n|\W)ComputerName =({host}[\w\-\.]+)\s*(\\n)?(\w+=|$)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (?i)(AM|PM))""",
    """(\\n|\W)Message=[^=]*?\Wuser\s*'\s*((({domain}[^\\]+)(\\)+))?({user}[\w\.\-]{1,40}\$?)'""",
    """(\\n|\W)SourceName =({service_name}[^=]+?)\s*(\\n)?(\w+=|$)""",
    """SourceName =({app}MSSQL)""",
    """\[CLIENT:\s+({src_ip}[a-fA-F\d:\.]+)\]""",
    """\WReason:\s*({failure_reason}[^:]+?)\s*\[""",
    """source_hostname":"({src_host}[^"]+)""",
    """EventCode=({event_code}\d+)""",
    """({event_name}Login failed)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```