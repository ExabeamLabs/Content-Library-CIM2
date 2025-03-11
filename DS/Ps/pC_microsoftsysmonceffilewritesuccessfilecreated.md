#### Parser Content
```Java
{
Name = "microsoft-sysmon-cef-file-write-success-filecreated"
Conditions = [
"""CEF:"""
"""|Microsoft Sysmon|Sysmon NXLog|"""
"""|SysmonTask-SYSMON_FILE_CREATE|File created|"""
]
ParserVersion = "v1.0.0"

cef-sysmon-file-write.Fields} [
    """cs2=({registry_value}[^=]+)\s+\w+="""
  
}
```