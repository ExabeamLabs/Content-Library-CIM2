#### Parser Content
```Java
{
Name = okta-amfa-kv-app-login-fail-signinfailure
    Vendor = Okta
    Product = Okta Adaptive MFA
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """|OKTA|OKTA Identity Provider|""","""|Sign-in Failure|"""]
    Fields = [
		"""start=({time}\d\d\d\d\-\d+\-\d+T\d+:\d+:\d+:\d+)""",
        """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
        """instance=({host}[^,]+)""",
        """user:\s({user}[^,]+)""",
        """msg=Sign-In Failed - ({failure_reason}[^:,]+)""",
        """cs3=({user_agent}.+?), \w+=""",
        """({app}Okta)"""
    ]
	ParserVersion = "v1.0.0"


}
```