#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-5058-1
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"EventID":"5058"""", """Key file operation""" ]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields} [
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

  ]

json-windows-events-2 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[^\\]+)""",
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[^\\]+))\\?"""",
    """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}[^\\]+))\\?"""",
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?"""",
    """event_id\\?"+:({event_code}\d+)""",
    """ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?"""",
    """WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}[^\s\\]+))\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\\]+)\\?"""",
    """ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?"""",
    """LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?"""",
    """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
  
}
```