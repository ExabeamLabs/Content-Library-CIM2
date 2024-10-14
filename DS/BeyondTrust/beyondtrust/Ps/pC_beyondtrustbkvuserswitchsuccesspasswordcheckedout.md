#### Parser Content
```Java
{
Name = beyondtrust-b-kv-user-switch-success-passwordcheckedout
    Vendor = BeyondTrust
    Product = BeyondTrust
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [ """sEventID="EVENT_ID_PASSWORD_CHECKED_OUT"""","""<Event"""]
    Fields = [
    """dtPostTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""",
    """sLoginName ="(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """sIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """sOriginatingSystem="({host}[^"]+)""",
    """sOriginatingSystem="({dest_host}[^"]+)""",
    """dwAppSpecificEventID="({event_code}[^"]+)""",
    """sMessage="checked-out password for\s*\([^\)]*\)'(({account_domain}[^\\\s']+)\\+)?({account}[^\\\s']+)""",
    """sEventID="({event_name}[^"]+)"""
    ]
        ParserVersion = "v1.0.0"
  

}
```