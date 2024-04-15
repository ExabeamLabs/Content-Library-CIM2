#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-file-write-success-threatindicators-2"
Conditions = [
"""threatIndicators"""
"""dproc=registry access event"""
"""destinationServiceName =CB Defense"""
""" attempted to modify """
""""eventType":"REGISTRY_ACCESS""""
]
ParserVersion = "v1.0.0"

cef-carbonblack-events-1.Fields} [
    """({result}failed)""",
    """"deviceName":"(({domain}[^\\\s"]+)\\+)?({src_host}[^\\\s"]+)"""",
  
}
```