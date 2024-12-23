#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-5058-1
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss"]
  ExtractionType = json
  Conditions = [ """"EventID":"5058"""", """Key file operation""" ]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields} [
    """"(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)""",
    """"hostname"+:"+({host}[^"]+)""",
    """({event_name}Key file operation)""",
    """({event_code}5058)""",
    """"Message":"({additional_info}[^"\\]+)""",
    """"Category":"({category}[^"]+)""",
# algorithm_name is removed
    """"KeyName":"({key_name}[^"]+)"+""",
    """"KeyFilePath":"({file_path}[^"]+)"+"""
    """"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}[^"]+)"""",
    """"Operation":"({operation}[^"]+)"""",
    """"Keywords":"({action}[^"]+)""",
    """exa_regex=({event_name}Key file operation)""",
    """exa_regex=({event_code}5058)""",
    """exa_json_path=$.EventData.KeyName,exa_field_name=key_name"""
    """exa_json_path=$.EventData.KeyFilePath,exa_field_name=file_path"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_json_path=$.EventData.Operation,exa_field_name=operation"""
    """exa_json_path=$.Keywords,exa_field_name=action"""
    """exa_regex="TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)"""
    """exa_regex="Message":"({additional_info}[^"\\]+)""",
  ]

json-windows-events-2 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?"""",
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?"""",
    """event_id\\?"+:({event_code}\d+)""",
    """ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\\]+)\\?"""",
    """ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?"""",
    """LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?"""",
    """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
  
}
```