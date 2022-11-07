#### Parser Content
```Java
{
Name = beyondtrust-privmgmt-kv-user-switch-success-passwordretrieved
    Vendor = BeyondTrust
    Product = BeyondTrust Privileged Identity
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [ """sEventID="EVENT_ID_PASSWORD_RETRIEVED"""","""<Event"""]
    Fields = [
    """dtPostTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""",
    """sLoginName ="(({domain}[^"]+)\\)?({user}[^"]+)""",
    """sAccountName"\s+value="({account}[^"]+)""",
    """sIpAddress="({src_ip}[^"]+)""",
    """sOriginatingSystem="({host}[^"]+)""",
    """sOriginatingSystem="({dest_host}[^"]+)""",
    """dwAppSpecificEventID="({event_code}[^"]+)""",
    """sNamespace"\s+value="({account_domain}[^"]+)"""
    ]
        ParserVersion = "v1.0.0"
  

}
```