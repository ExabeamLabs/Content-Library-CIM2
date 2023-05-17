#### Parser Content
```Java
{
Name = f5-f-kv-app-activity-common
 ParserVersion = v1.0.0
 Vendor = F5
 Product = F5 Access Policy Manager
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 start_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
 end_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
 Conditions = [ """:Common:""" ]
 Fields = [
   """:Common:({session_id}[^:]+)""",
   """domain' set to '({domain}[^\\\/\s'"]+)'""",
   """sAMAccountName =({account}[^\s'"\)]+)\)' ({result}\S+)""",
   """ Username '({account}[^\s'"]+)""",
   """ AD agent:\s*({user}[^\s]+).+? authenticate with '({account}[^\s'"]+)' ({result}\S+)""",
   """ authentication with '({account}[^\s']+)""",
   """ bytes in:\s*({bytes_in}\d+)""",
   """ bytes out:\s*({bytes_out}\d+)""",
   """ client IP ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """ request from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+) to ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)""",
   """ SID:\s*({user_sid}[^\s:]+)""",
   """ request:\s*({request}[^\s]+)""",
   """ Access policy result:\s*({result}[^\s]+)""",
   """ resource '?({resource}[^\s']+)""",
   """ Executed agent '([^\s']+)', return value ({result_code}\d+)""", # executed_agent is removed
   """at VIP\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
   """({start_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z).+?({end_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
   """sAMAccountName =({account}[^\s'"\)]+)\)'""",
   """ authentication with '({account}[^\s']+)'\s*({result}[^:]+):({additional_info}[^"]+)""",
   """platform' set to '({os}[^'"]+)'"""
   """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d+:\d+\s({vpn_server}[^\s]+)"""
   """hostname' set to '({src_host}[\w\-.]+)"""
 ]
  DupFields = [ "vpn_server->realm" ]


}
```