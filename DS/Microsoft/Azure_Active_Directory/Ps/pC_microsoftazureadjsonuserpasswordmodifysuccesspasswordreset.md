#### Parser Content
```Java
{
Name = microsoft-azuread-json-user-password-modify-success-passwordreset
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """activityDisplayName""","""ms:aad:audit""","""Self-service password reset flow activity progress""" ]
  Fields = [
    """"createdDateTime"+:\s*"+({time}[^"]+)""",
	"""ms:aad:audit"+,"+({host}[^"]+)""",
    """"userPrincipalName"+:\s*"+({email_address}[^"\s@]+@({email_domain}[^"\s@]+))""",
    """"ipAddress"+:\s*"+({src_ip}[A-Fa-f:\d.]+)""",
    """"activityDisplayName"+:\s*"+({operation}[^"]+)""",
	""""result"+:\s*"+"({result}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```