#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-file-write-success-threatindicators"
Conditions = [
"""threatIndicators"""
""""eventType":"FILE_CREATE""""
""" file was created """
]
ParserVersion = "v1.0.0"

cef-carbonblack-events-1.Fields} [
    """({result}failed)""",
    """"deviceName":"(({domain}[^\\\s"]+)\\+)?({src_host}[^\\\s"]+)"""",
  
}
```