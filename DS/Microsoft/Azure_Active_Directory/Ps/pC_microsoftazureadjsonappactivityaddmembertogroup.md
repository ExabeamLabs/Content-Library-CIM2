#### Parser Content
```Java
{
Name = microsoft-azuread-json-app-activity-addmembertogroup
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """activityDisplayName""","""ms:aad:audit""" ]
  Fields = [
    """"createdDateTime"+:\s*"+({time}[^"]+)""",
    """ms:aad:audit"+,"+({host}[^"]+)""",
    """"userPrincipalName"+:\s*"+({email_address}[^"\s@]+@({email_domain}[^"\s@]+))""",
    """"ipAddress"+:\s*"+({src_ip}[A-Fa-f:\d.]+)""",
    """"activityDisplayName"+:\s*"+({operation}[^"]+)""",
	""""result"+:\s*"+"({action}[^"]+)"""
    ]
	ParserVersion = "v1.0.0"


}
```