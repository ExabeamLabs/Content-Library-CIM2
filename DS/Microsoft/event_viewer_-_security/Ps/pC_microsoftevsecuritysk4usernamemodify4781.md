#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-user-name-modify-4781
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [""""event_id":4781""", """Microsoft-Windows-Security-Auditing""", """The name of an account was changed"""]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields}[
    """({event_name}The name of an account was changed)""",
    """"+OldTargetUserName"+:"+({old_user_name}[^"]+)""",
    """"+NewTargetUserName"+:"+({new_user_name}[^"]+)"""
  ]
    DupFields = [ "host-> dest_host" ]

json-windows-events-2 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}[\w\-.]]+)""",
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-]{1,40}\$?))\\?"""",
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