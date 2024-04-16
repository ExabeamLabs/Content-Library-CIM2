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
        """sIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """sLoginName ="(({domain}[^"]+)\\)?({user}[\w\.\-]{1,40}\$?)""",
        """sOriginatingSystem="({dest_host}[^"]+)"""
    ]
	ParserVersion = v1.0.0
  

}
```