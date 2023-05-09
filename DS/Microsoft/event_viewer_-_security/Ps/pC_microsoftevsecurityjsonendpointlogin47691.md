#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-4769-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = ["""A Kerberos service ticket was requested""", """Account Name""", """computer_name""", """event_id\":4769"""]
  Fields = ${DLWindowsParsersTemplates.json-windows-events-2.Fields}[
    """({event_name}A Kerberos service ticket was requested)""",
    """TargetUserName\\?"+:\\?"+((({user}[^@\s\\]+?)(?:@({domain}[^\\]+))?)|({email_address}[^@\s]+?@[^\s\.]+?\.[^\s\\]+?))\\?"""",
    """TargetDomainName\\?"+:\\?"+({web_domain}[^\\]+)""",
    """ServiceName\\?"+:\\?"+({dest_host}[^\s\\]+)""",
    """IpAddress\\?"+:\\?"+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?"""",
    """Status\\?"+:\\?"+({result_code}[^\s\\]+)""",
    """TicketOptions\\?"+:\\?"+({ticket_options}[^\s\\]+)""",
    """TicketEncryptionType\\?"+:\\?"+({ticket_encryption_type}[^\s\\]+)"""
    """"event_id[\\]?"+:({event_code}\d+)"""
 ]
 DupFields = ["dest_host->service_name"]

json-windows-events-2 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """@timestamp\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[^\\]+)""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({dest_host}[^\\]+)""",
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