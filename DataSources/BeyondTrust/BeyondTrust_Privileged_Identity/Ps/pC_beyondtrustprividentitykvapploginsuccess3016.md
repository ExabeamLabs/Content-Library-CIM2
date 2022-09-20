#### Parser Content
```Java
{
Name = beyondtrust-prividentity-kv-app-login-success-3016
    Vendor = BeyondTrust
    Product = BeyondTrust Privileged Identity
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [ """sEventID="EVENT_ID_WEBAPP_LOGIN"""","""<Event"""]
    Fields = [
        """\d+:\d+:\d+\s+({host}[^\s]+)\s+<Event""",
        """dtPostTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""",
        """sOriginatingApplicationName ="({app}[^"]+)""",
        """sIpAddress="({src_ip}[a-fA-F\d.:]+)""",
        """sLoginName ="(({domain}[^"]+)\\)?({user}[^"]+)""",
        """sOriginatingSystem="({src_host}[^"]+)"""
    ]
	ParserVersion = v1.0.0
  

}
```