#### Parser Content
```Java
{
Name = microsoft-mssql-json-app-login-fail-loginfailedforuser-1
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"provider_name":"MSSQLSERVER"""", """Login failed for user""" ]
  Fields = [
    """"@timestamp"\s*:\s*"({time}[^"]+)"""",
    """"computer_name"\s*:\s*"({host}[\w.-]+?)"""",
    """CLIENT:\s*({src_ip}[A-Fa-f\d.:]+)""",
    """({app}MSSQLSERVER)""",
    """"outcome":"({result}[^"]+)"""",
    """Reason:\s*({failure_reason}[^"\.\[]+)""",
    """"message":"({event_name}Login failed for user) '(({domain}[^\\:']+?)\\+)?({user}[\w\.\-]{1,40}\$?)'""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```