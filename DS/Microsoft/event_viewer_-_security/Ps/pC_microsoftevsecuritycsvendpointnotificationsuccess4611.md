#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-endpoint-notification-success-4611
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LogType="WLS"""", """EventID="4611"""" ]
    Fields = [
      """Computer="+({dest_host}[\w\-.]+)"""",
      """EventID="+({event_code}[^"]+)"""",
      """EventRecordID="+({event_id}[^"]+)"""",
      """LogonProcessName ="+({auth_process}[^"]+)"""",
      """SubjectUserName ="+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """SubjectUserSid="+({user_sid}[^"]+)"""",
      """SubjectDomainName ="+(?=\w)({domain}[^"]+)"""",
      """SubjectLogonId="+({login_id}[^"]+)""""
    ]
    DupFields = [ "user->src_user", "domain->src_domain" ]
  

}
```