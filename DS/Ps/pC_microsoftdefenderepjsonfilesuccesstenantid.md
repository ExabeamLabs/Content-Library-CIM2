#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-file-success-tenantid"
Conditions = [
""""Type":"AdvancedHuntingDeviceFileEvents_CL"""
"""TimeGenerated"""
"""TenantId"""
]
ParserVersion = "v1.0.0"

cef-sysmon-file-write.Fields} [
    """cs2=({registry_value}[^=]+)\s+\w+="""
    """cs1=({registry_path}[^=]*?\\+({registry_key}[^=\\\/]+?)\\+({registry_value}[^\\=]+))\s\w+="""
  
}
```