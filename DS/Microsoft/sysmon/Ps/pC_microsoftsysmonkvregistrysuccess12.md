#### Parser Content
```Java
{
Name = microsoft-sysmon-kv-registry-success-12
  Vendor = Microsoft
  Product = Sysmon
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """Event_ID="12"""", """][Event.System.TimeCreated _SystemTime=""", """Registry object added or deleted:""" ]
  Fields = [
    """Computer="({host}[^"]+)"""",
    """Event\.System\.TimeCreated _SystemTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""",
    """({event_name}Registry\sobject\sadded\sor\sdeleted)""",
    """Event_ID="({event_code}[^"]+)"""",
    """Keywords="({result}[^"]+)"""",
    """Image:\s+({process_path}({process_dir}[^\s]+)\\({process_name}[^\s]+\.?[^\s]*))""",
    """TargetObject:\s({file_path}[^\s]+\\({file_name}[^\s]+))""",
    """ProcessGuid:\s*\{({process_guid}[^}\s]+)""",
    """Event\.System\.Execution\s_ProcessID="({process_id}[^"]+)""",
    """Task="({operation}[^"]+)""",
    """Event\.System\.Security\s*_UserID="({user_sid}[^"]+)"""
  ]


}
```