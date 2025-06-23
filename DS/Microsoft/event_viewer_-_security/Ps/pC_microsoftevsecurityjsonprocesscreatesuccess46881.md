#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-create-success-4688-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [
""","EventID":4688,""", 
"""A new process has been created"""
  ]
  Fields = [
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"Computer":"({host}[\w\-.]+)"""",
      """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """"Account":"(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """({event_code}4688)""",
      """({event_name}A new process has been created)""",
      """"Activity":"({event_name}[^"]+)""",
      """"Hostname":"({host}[\w\-.]+)""",
      """"CommandLine":"\s*({process_command_line}[^"]+)""",
      """"NewProcessId":"({process_guid}[^"]+)""",
      """"NewProcessName":"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
      """Creator Subject:.+?Account Name:\s*((\\)*(\\r|\\t|\\n))*(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))((\\)*(\\r|\\t|\\n))*\s*Account Domain:((\\)*(\\r|\\t|\\n))*\s*(?:-|({domain}.+?))((\\)*(\\r|\\t|\\n))*\s*Logon ID:((\\)*(\\r|\\t|\\n))*\s*({login_id}[^\\\s]+)"""
      """"SubjectLogonId":"({login_id}[^"]+)""",
      """"SubjectUserName":"(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """"SubjectDomainName":"(-|({domain}[^"]+?))""""
      """"ComputerName":"({host}[\w\-.]+)"""
      """"ParentProcessName":"({parent_process_path}({parent_process_dir}[^"]*?[\\\/]+)?({parent_process_name}[^"\\\/]+))""""
      """exa_json_path=$.TimeGenerated,exa_field_name=time"""
      """exa_json_path=$.Computer,exa_field_name=host"""
      """exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """exa_json_path=$.Account,exa_field_name=domain"""
      """exa_regex=({event_code}4688)"""
      """exa_regex=({event_name}A new process has been created)"""
      """exa_json_path=$.Activity,exa_field_name=event_name"""
      """exa_json_path=$.Hostname,exa_field_name=host"""
      """exa_json_path=$.CommandLine,exa_field_name=process_command_line"""
      """exa_json_path=$..NewProcessId,exa_field_name=process_guid"""
      """exa_json_path=$..NewProcessName,exa_regex=({process_path}({process_dir}[^"]+[\\\/]+)?({process_name}[^"\\\/]+))"""
      """exa_regex="Creator Subject:.+?Account Name:\s*((\\)*(\\r|\\t|\\n))*(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))((\\)*(\\r|\\t|\\n))*\s*Account Domain:((\\)*(\\r|\\t|\\n))*\s*(?:-|({domain}.+?))((\\)*(\\r|\\t|\\n))*\s*Logon ID:((\\)*(\\r|\\t|\\n))*\s*({login_id}[^\\\s]+)"""
      """exa_json_path=$..SubjectLogonId,exa_field_name=login_id"""
      """exa_json_path=$..SubjectUserName,exa_field_name=user"""
      """exa_json_path=$..SubjectDomainName,exa_field_name=domain"""
      """exa_json_path=$..ComputerName,exa_field_name=host"""
      """exa_json_path=$..ParentProcessName,exa_regex=({parent_process_path}({parent_process_dir}[^"]+[\\\/]+)?({parent_process_name}[^"\\\/]+))"""
  ]
  DupFields = [ "host->src_host", "user->src_user", "domain->src_domain" ]


}
```