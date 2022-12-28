#### Parser Content
```Java
{
Name = progress-pdatabase-str-endpoint-login-success-742
  Vendor = Progress
  Product = Progress Database
  TimeFormat = "yyyy-MM-dd'@'HH:mm:ss.SSSZ"
  Conditions = [ """ T-""", """ P-""", """(742)""", """ Login """ ]
  Fields = [
  """:\d\d:\d\d\s+({src_host}[^\s]+)\s+\[({time}\d\d\d\d\/\d\d\/\d\d@\d\d:\d\d:\d\d\.\d\d\d-\d\d\d\d)\]\s+({process_id}[^\s]+)\s+({thread_id}[^\s]+)\s+({severity}[^\s]+)\s+({service_name}TSRV)\s+\d:\s*\(({event_code}742)\)\s+({additional_info}({event_name}Login)[^,]+),\s+userid\s({user}[^\s]+)[^,]+,\son\s({dest_host}[^\s]+)\s[^"]+?({dest_ip}[\da-fA-F.:]+?)\.?\s+"?$"""
  ]
  ParserVersion = "v1.0.0"


}
```