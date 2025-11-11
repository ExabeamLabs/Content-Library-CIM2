#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-windows"
Conditions = [
""""data.id":"4776""""
""""type":"wazuh-alerts""""
""""decoder.parent":"windows""""
]
ExtractionType = json
ParserVersion = "v1.0.0"

json-windows-events-2-aa.Fields}[
    """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """(?:winlog\.)?computer_name\\?"+:\\?"+({host}[\w\-.]+)""",
    """WorkstationName\\?"+:\\?"+(?:-|({src_host}({src_host_windows}[^\s\\]+)))\\?"""",
    """SubjectUserName\\?"+:\\?"(?:-|LOCAL SYSTEM|({src_user}[^\\]+))\\?"""",
    """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\]+)))\\?"""",
    """SubjectUserSid\\?"+:\\?"+({dest_user_sid}[^\\]+)\\?"""",
    """SubjectDomainName\\?"+:\\?"({domain}({src_domain}[^\\"]+))\\?"""",
    """SubjectLogonId\\?"+:\\?"({login_id}[^\\]+)\\?"""",
    """TargetSid\\?"+:\\?"({user_sid}[^\\]+)\\?"""",
    """TargetUserName\\?"+:\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?"""",
    """TargetDomainName\\?"+:\\?"({domain}[^\s\\]+)\\?"""",
    """TargetSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?"""",
    """TargetUserName\\?"+:\\?"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """TargetDomainName\\?"+:\\?"({src_host}[^\s\\]+)\\?"""",
    """"message\\*":\\*"({event_name}A user account was locked out)"""
  
}
```