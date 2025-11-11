#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-create-success-4688-2
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"event_id""", """4688""", """A new process has been created""" ]
    Fields = [
      """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
      """"@timestamp"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
      """"Account"*:"*(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """({event_code}4688)""",
      """"Activity"*:"*({event_name}[^"]+)""",
      """"hostname"*:"*({host}[\w\-.]+)""",
      """"hostname"*:"*({host}({src_host}[\w\-.]+))""",
      """"CommandLine":\s*"\s*({process_command_line}[^\n]+?)\s*"?,"""",
      """"NewProcessId"*:"*({process_guid}[^"]+)""",
      """"NewProcessName"*:"*({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
      """"SubjectLogonId"*:"*({login_id}[^"]+)""",
      """"SubjectUserName"*:"*(-|SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""""
      """"SubjectDomainName"*:"*(-|({src_domain}({domain}[^"]+?)))""""
      """exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """exa_regex=\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
      """exa_regex="@timestamp"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",      
      """exa_json_path=$.Account,exa_regex=(({src_domain}({domain}[^"]+?))[\\\/]+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """exa_regex=({event_code}4688)""",
      """exa_json_path=$.Activity,exa_field_name=event_name"""
      """exa_json_path=$.hostname,exa_field_name=host"""
      """exa_json_path=$.hostname,exa_field_name=src_host"""
      """exa_json_path=$.CommandLine,exa_field_name=process_command_line"""
      """exa_json_path=$.NewProcessId,exa_field_name=process_guid"""
      """exa_json_path=$.NewProcessName,exa_regex=({process_path}({process_dir}[^"]+[\\\/]+)?({process_name}[^"\\\/]+))""",
      """exa_json_path=$.SubjectLogonId,exa_field_name=login_id"""
      """exa_json_path=$.SubjectUserName,exa_field_name=user"""
      """exa_json_path=$.SubjectDomainName,exa_field_name=domain"""
      """exa_json_path=$.SubjectUserName,exa_field_name=src_user"""
      """exa_json_path=$.SubjectDomainName,exa_field_name=src_domain"""
    ]
  

}
```