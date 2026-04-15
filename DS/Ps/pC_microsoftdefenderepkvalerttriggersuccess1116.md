#### Parser Content
```Java
{
Name = "microsoft-defenderep-kv-alert-trigger-success-1116"
Conditions = [ """<EventID>1116</EventID>""", """<Channel>Microsoft-Windows-Windows Defender/Operational</Channel>""", """<Data Name""", """>Microsoft Defender Antivirus</Data>"""]
ParserVersion = "v1.0.0"

json-windows-events-2.Fields}[
    """"TargetDomainName"+:"+({account_domain}[^"]+)""",
    """"(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)""",
    """"TargetUserName"+:"+({dest_user}[^"]+)""",
    """"user"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"+SubjectDomainName"+:"+({src_domain}[^"]+)""",
    """"+SubjectUserName"+:"+(SYSTEM|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"hostname"+:"+({host}[^"]+)""",
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)""",
    """TargetUserName\\?"+:\\?"(?:-|(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"""",
    """IpAddress\\?"+:\\?"(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\?"""",
    """Status\\?"+:\\?"({failure_code}({result_code}[\w\-]+))\\?"""",
    """TargetDomainName\\?"+:\\?"(?:-|({dest_domain}({domain}[^\s\\]+?)))\\?"""",
    """TargetSid\\?"+:\\?"({dest_user_sid}({user_sid}[^\\"]+))\\?""""
    """"event_id[\\]?"+:({event_code}\d+)"""
  
}
```