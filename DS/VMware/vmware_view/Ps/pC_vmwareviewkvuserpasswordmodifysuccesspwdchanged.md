#### Parser Content
```Java
{
Name = "vmware-view-kv-user-password-modify-success-pwdchanged"
Vendor = "VMware"
Product = "VMware View"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""" View - """
"""BROKER_USERCHANGEDPASSWORD"""
"""Severity="AUDIT_SUCCESS""""
]
Fields = [
"""\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+\d+\s+"""
"""\s+({dest_host}[^\s]+)\s+View - """
"""\s+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
"""UserDisplayName =\"(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
]
ParserVersion = "v1.0.0"


}
```