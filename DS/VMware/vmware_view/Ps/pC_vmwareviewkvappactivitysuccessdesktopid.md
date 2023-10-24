#### Parser Content
```Java
{
Name = "vmware-view-kv-app-activity-success-desktopid"
Vendor = "VMware"
Product = "VMware View"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""" View - """
"""Severity=""""
"""DesktopId=""""
]
Fields = [
"""\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+\d+\s+"""
"""({app}View)"""
"""\s+({dest_host}[^\s]+)\s+View - """
"""\s+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
"""UserDisplayName ="(({domain}[^\\]+)\\+)?\\*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
"""MachineName ="({dest_host}[^"]+)""""
"""EventType="({operation}[^"]+)""""
"""DesktopId="({object}[^"]+)""""
"""_USER_.+?UserDisplayName ="([^\\]+\\+)?({object}[^"]+)""""
"""\] ({additional_info}.+?)\s*$"""
"""Severity="({alert_severity}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```