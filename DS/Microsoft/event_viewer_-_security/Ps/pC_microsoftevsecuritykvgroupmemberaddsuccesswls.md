#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-wls"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
"""LogType="WLS""""
"""MemberName ="""
"""MemberSid="""
]
Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""Computer="+({dest_host}({host}[^"]+))""""
""""({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)"""
"""EventID="+({group_type}({event_code}[^"]+))""""
"""EventRecordID="+({event_id}[^"]+)""""
"""SubjectUserName ="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""SubjectUserSid="+({user_sid}[^"]+)""""
"""SubjectDomainName ="+({src_domain}({domain}[^"]+))""""
"""SubjectLogonId="+({login_id}[^"]+)""""
"""TargetUserName ="+({group_name}[^"]+)""""
"""TargetDomainName ="+({group_domain}[^"]+)""""
"""MemberSid="+(({dest_user_sid}S-\d+-[^"]+)|({account_id}[^"]+))""""
"""MemberName ="+({user_dn}[^"]+)""""
"""MemberName ="+.*?OU=({user_ou}[^,]+)?"""
"""TargetSid="({group_id}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```