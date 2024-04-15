#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-file-write-success-threatindicators-1"
Conditions = [
"""threatIndicators"""
""""eventType":"REGISTRY_ACCESS""""
""" attempted to modify """
]
ParserVersion = "v1.0.0"

cef-carbonblack-events-1.Fields} [
    """({result}failed)""",
    """"deviceName":"(({domain}[^\\\s"]+)\\+)?({src_host}[^\\\s"]+)"""",
  
}
```