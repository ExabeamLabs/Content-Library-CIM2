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
    """"ipAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"activityDisplayName"+:\s*"+({operation}[^"]+)""",
	""""result"+:\s*"+"({action}[^"]+)"""
    ]
	ParserVersion = "v1.0.0"


}
```