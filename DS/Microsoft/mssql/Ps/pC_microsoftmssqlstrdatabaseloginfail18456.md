#### Parser Content
```Java
{
Name = microsoft-mssql-str-database-login-fail-18456
  Vendor = Microsoft
  Product = MSSQL
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 18456 """, """ Login failed """,""" MSWinEventLog """ ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}18453)""",
    """({event_name}Login failed)""",
    """database '({db_name}[^']+)""",
    """user '(N\/A|(({domain}[^\\']+)\\+)?({user}[^\s']+))""",
    """CLIENT:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = ["user->db_user"]


}
```