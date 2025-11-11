#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-user-create-success-usercreated
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [  """A user account was created""", """"Type":"AADDomainServicesAccountManagement"""", """"Azure"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}(\.\d{1,8})?Z)""""
    """({event_name}A user account was created)"""
    """"SamAccountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"SubjectUserSid":"({user_sid}[^"]+)"""
    """"Category":"({category}[^"]+)"""
    """({event_code}4720)"""
    """"TargetSid":"+({dest_user_sid}[^"]+)"""
    """"UserPrincipalName":"({user_upn}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+))?)""""
    """"SubjectLogonId":"({login_id}[^\s"]+)"""
    """"TargetUserName":"({dest_user}({account_name}[^"]+))"""
    """"TargetDomainName":"({account_domain}[^"]+)"""
    """"DisplayName":"({full_name}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```