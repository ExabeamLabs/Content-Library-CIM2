#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-wls"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""MemberName ="""
"""MemberSid="""
]
Fields = [
"""Computer="+({host}[^"]+)""""
""""({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)"""
"""EventID="+({event_code}[^"]+)""""
"""EventRecordID="+({event_id}[^"]+)""""
"""SubjectUserName ="+({user}[^"]+)""""
"""SubjectUserSid="+({user_sid}[^"]+)""""
"""SubjectDomainName ="+({domain}[^"]+)""""
"""SubjectLogonId="+({login_id}[^"]+)""""
"""TargetUserName ="+({group_name}[^"]+)""""
"""TargetDomainName ="+({group_domain}[^"]+)""""
"""MemberSid="+({account_id}[^"]+)""""
"""MemberName ="+({user_dn}[^"]+)""""
"""MemberName ="+.*?OU=({user_ou}[^,]+)?"""
"""TargetSid="({group_id}[^"]+)"""
]
DupFields = [
"event_code->group_type"""
"host->dest_host"""
]
ParserVersion = "v1.0.0"


}
```