#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-password-modify-4723-3
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LogType="WLS"""", """EventID="4723"""" ]
    Fields = [
      """Computer="+({host}[^"]+)"""",
      """({time}\w+ \d+ \d\d:\d\d:\d\d)""",
      """Keywords="+({result}[^"]+)"""",
      """EventID="+({event_code}[^"]+)"""",
      """EventRecordID="+({event_id}[^"]+)"""",
      """SubjectUserName ="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """SubjectDomainName ="+({src_domain}({domain}[^"]+))"""",
      """SubjectLogonId="+({login_id}[^"]+)"""",
      """SubjectUserSid="+({user_sid}[^"]+)"""",
      """TargetSid="+({dest_user_sid}[^"]+)"""",
      """TargetDomainName ="+({dest_domain}[^"]+)"""",
      """TargetUserName ="+({dest_user}[^"]+)"""",
      """ProviderGuid="+({process_guid}[^"]+)""""
    ]
    ParserVersion = "v1.0.0"
  

}
```