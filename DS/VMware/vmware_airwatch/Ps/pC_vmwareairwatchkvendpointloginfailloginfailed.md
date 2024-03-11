#### Parser Content
```Java
{
Name = vmware-airwatch-kv-endpoint-login-fail-loginfailed
  ParserVersion = "v1.0.0"
  Conditions = [ """AirWatch""", """Event Timestamp:""", """ConsoleEvent: AdminUserLoginAttemptFailed""" ]
  Fields = ${VMWareParsersTemplates.airwatch-app-activity.Fields}[
    """({action}AdminUserLoginAttemptFailed)"""
  ]

airwatch-app-activity = {
    Vendor = VMware
    Product = VMware AirWatch
    TimeFormat = "MMMM dd, yyyy HH:mm:ss"
    Fields = [
      """Timestamp: ({time}\w+\s\d+,\s\d{4}\s(\d{2}:){2}\d{2})""",
      """Event Type:\s*({event_name}[^=]+?)\s*User:""",
      """User:\s*((({domain}[^\\]+?)\\+)?({user}[^:]+?))\s*Event Source:"""
    ]
     DupFields = ["event_name->operation"
}
```