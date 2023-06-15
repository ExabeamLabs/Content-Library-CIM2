#### Parser Content
```Java
{
Name = okta-amfa-kv-app-login-success-singlesignon
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """|OKTA|OKTA Identity Provider|""","""|Application Access|""","""msg=User performed single sign on to app"""]
  Fields = [
	"""start=({time}\d\d\d\d\-\d+\-\d+T\d+:\d+:\d+:\d+)""",
	"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	"""instance=({host}[^,]+)""",
    """duid=({user}[^,]+)""",
    """duid=[^@,]+@({domain}[^,.]+)""",
    """destinationServiceName =({app}[^,]+)""",
    """cs3=({user_agent}.+?), \w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```