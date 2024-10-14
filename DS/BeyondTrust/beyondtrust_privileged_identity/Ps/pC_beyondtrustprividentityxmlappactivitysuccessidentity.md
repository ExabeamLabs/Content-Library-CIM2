#### Parser Content
```Java
{
Name = "beyondtrust-prividentity-xml-app-activity-success-identity"
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
Conditions = [
"""sEventID="EVENT_ID_JOB_ACCOUNT_ELEVATED""""
"""sOriginatingApplicationName ="Privileged Identity""""
"""<Event """
]
Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""dtPostTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""sEventID="({operation}[^"]+)"""
"""\(running as user (({account_domain}[^\s\\]+)\\+)?({account}[^\s\\\)]+)\)"""
""""AccountToElevate"\s+value="(({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""group '({object}[^\']+)' on system """
""""TargetSystem"\s+value="({dest_host}[^"]+)"""
"""OriginatingApplicationName ="({app}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```