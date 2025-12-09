#### Parser Content
```Java
{
Name = "tanium-ep-json-alert-trigger-success-accountenumeration"
Product = "Tanium Threat Response"
Vendor = "Tanium"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Intel Id"""
"""Intel Type"""
"""Intel Name"""
"""Intel Labels"""
]
Fields = [
  """"Alert Id":\s*"({alert_id}[^"]+)""""
  """"Timestamp":\s*"({time}[^"]+)""""
  """"Computer Name":\s*"({src_host}[^"]+)""""
  """"Computer IP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
  """"Intel Type":\s*"({alert_type}[^"]+)""""
  """"Intel Name":\s*"({alert_name}[^"]+)""""
  """"Match Details":\{"match":\{[^\$]+?"properties"[^\$]+?"file"[^\]]+?"fullpath":"({path}({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+)))""""
  """"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?args\\?"+:"*\\*"+({process_command_line}[^,\]]+?)\\?\s*","""
  """"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?md5\\?"+:"*\\*"+({hash_md5}[^,\]]+?)\\?\s*","""
  """"user":"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:SYSTEM|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"\},"source"""
  """"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?"user":"+(?:(?:NT AUTHORITY|({domain}[^\\"]+))\\+)?(?:({user}SYSTEM|LOCAL SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """"Match Details":\{"match":\{[^\$]+?"properties"[^\]]+?"parent":\s*\{[^\]]+?file"[^\]]+?"fullpath":"(({parent_process_path}({parent_process_dir}[^"]+)\\+({parent_process_name}[^"]+)))"""
]
ParserVersion = "v1.0.0"


}
```