#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-lock-success-4740-2
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LogType="WLS"""", """EventID="4740"""" ]
    Fields = [
      """Computer="({host}[^"]+)"""",
      """EventID="({event_code}[^"]+)"""",
      """EventRecordID="({event_id}[^"]+)"""",
      """SubjectUserName ="({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """SubjectDomainName ="({src_domain}[^"]+)"""",
      """SubjectUserName ="({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """SubjectDomainName ="({domain}[^"]+)"""",
      """SubjectUserSid="({user_sid}[^"]+)""""
      """ProviderGuid="({process_guid}[^"]+)""",
      """SubjectLogonId="({login_id}[^"]+)"""",
      """TargetUserSid="({dest_user_sid}[^"]+)"""",
      """TargetDomainName ="({domain}[^"]+)"""",
      """TargetUserName ="({user}[\w\.\-]{1,40}\$?)""""
      """TargetDomainName ="({domain}({src_domain}[^"]+))"""",
      """TargetUserName ="({dest_user}[^"]+)""""
    ]
	ParserVersion = "v1.0.0"
  

}
```