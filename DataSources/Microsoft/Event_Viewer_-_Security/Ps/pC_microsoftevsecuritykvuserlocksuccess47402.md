#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-lock-success-4740-2
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LogType="WLS"""", """EventID="4740"""" ]
    Fields = [
      """Computer="+({src_host}[^"]+)"""",
      """EventID="+({event_code}[^"]+)"""",
      """EventRecordID="+({event_id}[^"]+)"""",
      """SubjectUserName ="+({caller_user}[^"]+)"""",
      """SubjectDomainName ="+({caller_domain}[^"]+)"""",
      """SubjectLogonId="+({login_id}[^"]+)"""",
      """TargetUserSid="+({user_sid}[^"]+)"""",
      """TargetDomainName ="+({src_host}[^"]+)"""",
      """TargetUserName ="+({user}[^"]+)""""
    ]
    DupFields=[ "caller_domain->domain" ]
	ParserVersion = "v1.0.0"
  

}
```