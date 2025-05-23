#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-activity-success-26401
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventID="26401"""", """MOMSDK_Service_Security""", """RecordNumber=""", """EventType=""", """Channel=""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)\-\d+:\d+\s({host}[^\s]+)""",
    """AccountName ="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"\sUserID="({user_sid}[^"]+)"\sAccountType="User""""
  ]

windows-system-info = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Fields = [
    """"EventID":"({event_code}\d+)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserName":"(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"SubjectDomainName":"(-|({domain}[^"]+))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
  ]
  DupFields = [ "user->src_user" , "domain->src_domain" 
}
```