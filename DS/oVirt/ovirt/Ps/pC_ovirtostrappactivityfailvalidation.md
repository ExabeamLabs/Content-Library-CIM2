#### Parser Content
```Java
{
Name = "ovirt-o-str-app-activity-fail-validation"
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" failed for user """
"""ovirt"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
"""Validation of action '({operation}[^']+)"""
"""failed for user ({user}[\w\.\-]{1,40}\$?)(@({domain}[^@\s]+))?.+Reasons:"""
"""Reasons:\s*({failure_reason}[^"]+?)\s*$"""
"""({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```