#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-user-create-success-usercreated
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """A user account was created""", """destinationServiceName =Azure""" ]
  Fields = [
    """({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,8}Z)"""
    """({event_name}A user account was created)""",
    """"SamAccountName":"({user}[^"]+)""""
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"Category":"({category}[^"]+)"""
    """({event_code}4720)"""
    """"TargetSid":"+({dest_user_sid}[^"]+)"""
    """"UserPrincipalName":"({email_address}[^"\s@]+@[^"\s@]+?)""""
    """"SubjectLogonId":"({login_id}[^\s"]+)""",
    """"TargetUserName":"({account_name}[^"]+)"""
    """"TargetDomainName":"({account_domain}[^"]+)"""
  ]
  DupFields = [
"account_name->dest_user"
]
  ParserVersion = "v1.0.0"


}
```