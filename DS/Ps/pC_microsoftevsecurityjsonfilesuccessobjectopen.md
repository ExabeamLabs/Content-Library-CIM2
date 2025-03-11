#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-objectopen"
Conditions = [
"""EventCode=560"""
"""Message=Object Open"""
]
ParserVersion = "v1.0.0"

cef-sysmon-file-write.Fields} [
    """cs2=({registry_value}[^=]+)\s+\w+="""
  
}
```