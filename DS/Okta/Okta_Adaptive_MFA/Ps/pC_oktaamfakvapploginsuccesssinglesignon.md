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
	"""src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
	"""instance=({host}[^,]+)""",
    """duid=({user}[^,]+)""",
    """duid=[^@,]+@({domain}[^,.]+)""",
    """destinationServiceName =({app}[^,]+)""",
    """cs3=({user_agent}.+?), \w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```