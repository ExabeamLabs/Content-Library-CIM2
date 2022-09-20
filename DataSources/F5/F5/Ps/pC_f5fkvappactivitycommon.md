#### Parser Content
```Java
{
Name = f5-f-kv-app-activity-common
 ParserVersion = v1.0.0
 Vendor = F5
 Product = F5
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """:Common:""" ]
 Fields = [
   """:Common:({session_id}[^:]+)""",
   """ set to '({user}[^\\\/\s'"]+)'""",
   """sAMAccountName =({account}[^\s'"\)]+)\)' ({result}\S+)""",
   """ Username '({account}[^\s'"]+)""",
   """ AD agent:\s*({user}[^\s]+).+? authenticate with '({account}[^\s'"]+)' ({result}\S+)""",
   """ authentication with '({account}[^\s']+)""",
   """ bytes in:\s*({bytes_in}\d+)""",
   """ bytes out:\s*({bytes_out}\d+)""",
   """ client IP ({src_ip}[A-Fa-f:\d.]+)""",
   """ request from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+) to ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)""",
   """ SID:\s*({user_sid}[^\s:]+)""",
   """ request:\s*({request}[^\s]+)""",
   """ Access policy result:\s*({result}[^\s]+)""",
   """ resource '?({resource}[^\s']+)""",
   """ Executed agent '([^\s']+)', return value ({result_code}\d+)""", # executed_agent is removed
   """at VIP\s*({dest_ip}[A-Fa-f:\d.]+)""",
   """({start_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?({end_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
   """sAMAccountName =({account}[^\s'"\)]+)\)'""",
   """ authentication with '({account}[^\s']+)'\s*({result}[^:]+):({additional_info}[^"]+)"""
 ]


}
```