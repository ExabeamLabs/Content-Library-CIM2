#### Parser Content
```Java
{
Name = progress-pdatabase-str-endpoint-login-success-742
  Vendor = Progress
  Product = Progress Database
  TimeFormat = "yyyy-MM-dd'@'HH:mm:ss.SSSZ"
  Conditions = [ """ T-""", """ P-""", """(742)""", """ Login """ ]
  Fields = [
  """:\d\d:\d\d\s+({src_host}[^\s]+)\s+\[({time}\d\d\d\d\/\d\d\/\d\d@\d\d:\d\d:\d\d\.\d\d\d-\d\d\d\d)\]\s+({process_id}[^\s]+)\s+({thread_id}[^\s]+)\s+({severity}[^\s]+)\s+({service_name}TSRV)\s+\d:\s*\(({event_code}742)\)\s+({additional_info}({event_name}Login)[^,]+),\s+userid\s({user}[\w\.\-]{1,40}\$?)[^,]+,\son\s({dest_host}[^\s]+)\s[^"]+?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\.?\s+"?$"""
  ]
  ParserVersion = "v1.0.0"


}
```