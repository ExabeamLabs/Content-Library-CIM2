#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4769-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = ["""A Kerberos service ticket was requested""", """Account Name""", """computer_name""", """event_id\":4769"""]
  Fields = ${WindowsParsersTemplates.json-windows-events-2-aa.Fields}[
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}[^\\]+))\\?"""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)""",
    """WorkstationName\\?"+:\\?"+(?:-|({src_host}({src_host_windows}[^\s\\]+)))\\?"""",
    """({event_name}A Kerberos service ticket was requested)""",
    """TargetUserName\\?"+:\\?"+((({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({dest_domain}({domain}[^\\]+))?))|({user_upn}[^@\s]+?@[^\s\.]+?(\.[^\s\\]+?)?))\\?"""",
    """TargetDomainName\\?"+:\\?"+({web_domain}[^\\]+)""",
    """ServiceName\\?"+:\\?"+({dest_host}[\w\-.]+\$)""",
    """ServiceName\\?"+:\\?"+({service_name}[\w\-.]+)""",
    """IpAddress\\?"+:\\?"+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\s\\]+)""",
    """TicketOptions\\?"+:\\?"+({ticket_options}[^\s\\]+)""",
    """TicketEncryptionType\\?"+:\\?"+({ticket_encryption_type}[^\s\\]+)"""
    """"event_id[\\]?"+:({event_code}\d+)"""
 ]

json-windows-events-2-aa = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """SubjectUserSid\\?"+:\\?"+({user_sid}[^\\]+)\\?"""",
    """SubjectLogonId\\?"+:\\?"+({login_id}[^\\]+)\\?"""",
    """event_id\\?"+:({event_code}\d+)""",
    """ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\\]+)\\?"""",
    """ProcessId\\?"+:\\?"+({process_id}[^:\\]+?)\\?"""",
    """LogonProcessName\\?"+:\\?"+({auth_process}[^\s\\]+)\s*\\?"""",
    """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^\s\\]+)\\?""""
  
}
```