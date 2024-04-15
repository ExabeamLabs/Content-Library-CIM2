#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-network-session-success-netconn"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Sysmon"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""Microsoft-Windows-Sysmon"""
"""Network connection detected"""
""""AccountName":""""
  ]
  Fields = [
"""\"UtcTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\"TargetFilename\":\"({file_path}({file_dir}[^\"]*?[\\\/]+)?({file_name}[^\"\\\/]+?(\.({file_ext}\w+))?))\""""
"""\"Protocol\":\"({protocol}[^\"]+)"""
"""\"Domain\":\"(NT AUTHORITY|({domain}[^\"]+))"""
"""\"AccountName\":\"((?i)SYSTEM|({user}[^\"]+))"""
"""\"ProcessGuid\":\"({process_guid}[^\"]+)"""
"""ProcessId:\s*({process_id}\d+)"""
"""\"LogonId\":\"({login_id}[^\"]+)"""
"""\"Hostname\":\"({host}[^\"]+)"""
"""\"SourceIp\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"SourceHostname\":\"(-|({src_host}[^\"]+))"""
"""\"SourcePort\":\"({src_port}\d+)"""
"""\"DestinationIp\":\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\"DestinationHostname\":\"({dest_host}[^\"]+)"""
"""\"DestinationPort\":\"({dest_port}\d+)"""
"""\"EventID\":({event_code}\d+)"""
"""\"User\":\"((NT AUTHORITY|({domain}[^\\]+))[\\]+)?((?i)SYSTEM|({user}[^\"]+))\""""
"""\"Image\":\"({process_path}({process_dir}[^\"]*?[\\\/]+)?({process_name}[^\"\\\/]+))\""""
  ]
  DupFields = [
"host->dest_host"
"process_path->path"
  ]


}
```