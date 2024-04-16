#### Parser Content
```Java
{
Name = beyondtrust-b-kv-user-switch-success-accessgranted
    Vendor = BeyondTrust
    Product = BeyondTrust
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [ """sEventID="EVENT_ID_PASSWORD_ACCESS_GRANTED"""","""<Event"""]
    Fields = [
        """\d+:\d+:\d+\s+({host}[^\s]+)\s+<Event""",
        """dtPostTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""",
        """sEventID="({event_code}[^"]+)""",
        """sIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """sLoginName ="(({domain}[^"\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
        """key="sNamespace"\s+value="({safe_value}[^"]+)""",
        """key="sSystemName"\s+value="({dest_service_name}[^"]+)""",
        """key="sAccountName"\s+value="({account}[^"]+)""",
        """sOriginatingSystem="({dest_host}[^"]+)"""
    ]
        ParserVersion = "v1.0.0"
  

}
```