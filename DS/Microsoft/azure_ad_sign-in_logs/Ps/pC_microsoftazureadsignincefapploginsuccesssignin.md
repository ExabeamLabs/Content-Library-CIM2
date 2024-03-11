#### Parser Content
```Java
{
Name = microsoft-azureadsignin-cef-app-login-success-signin
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure AD Sign-In Logs 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """CEF:""", """destinationServiceName =Azure""", """"OperationName":"User Risk Detection"""", """"Activity":"signin"""", """"RiskDetail":"aiConfirmedSigninSafe"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
	"""destinationServiceName =({app}Azure)""",
	"""OperationName":"({operation}[^"]+)""",
	"""({event_name}signin)""",
	""""IpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
	"""CallerIpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
	""""UserPrincipalName":"({email_address}[^"\s@]+@[^"\s@]+)""",
	""""UserDisplayName":"({full_name}({first_name}[^\s"]+)\s+({last_name}[^"]+))""",
	""""userAgent\\?",\\"?Value\\?":\\?"({user_agent}[^"\\]+)\\?"""",
	""""RiskDetail":"({additional_info}[^"]+)"""
  ]


}
```