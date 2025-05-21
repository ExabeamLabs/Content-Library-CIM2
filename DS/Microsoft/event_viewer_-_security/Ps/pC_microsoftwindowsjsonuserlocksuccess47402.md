#### Parser Content
```Java
{
Name = microsoft-windows-json-user-lock-success-4740-2
  ParserVersion = v1.0.0
  Conditions = [ """Account That Was Locked Out""", """event_id\":4740""", """computer_name""" ]
  Fields = ${WindowsParsersTemplates.json-windows-events-2-aa.Fields}[
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)""",
    """WorkstationName\\?"+:\\?"+(?:-|({src_host}({src_host_windows}[^\s\\]+)))\\?"""",
    """SubjectUserName\\?"+:\\?"({src_user}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"({src_domain}[^\\]+)\\?"""",
    """SubjectLogonId\\?"+:\\?"({login_id}[^\\]+)\\?"""",
    """TargetSid\\?"+:\\?"({user_sid}[^\\]+)\\?"""",
    """TargetUserName\\?"+:\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?"""",
    """TargetDomainName\\?"+:\\?"({src_host}[^\s\\]+)\\?"""",
    """"message\\*":\\*"({event_name}A user account was locked out)"""
  ]
  DupFields=[ "src_domain->domain", "user_sid->dest_user_sid", "user->dest_user" ]

json-windows-events-2-aa = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}[^\\]+))\\?"""",
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?"""",
    """event_id\\?"+:({event_code}\d+)""",
    """ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\\]+)\\?"""",
    """ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?"""",
    """LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?"""",
    """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
  
}
```