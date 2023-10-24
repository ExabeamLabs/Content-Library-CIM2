#### Parser Content
```Java
{
Name = vmware-airwatch-kv-endpoint-login-success-adminuserloggedin
  ParserVersion = "v1.0.0"
  Conditions = [ """AirWatch""", """Event Timestamp:""", """ConsoleEvent: AdminUserLoggedIn""" ]
  Fields = ${VMWareParsersTemplates.airwatch-app-activity.Fields}[
    """({result}AdminUserLoggedIn)"""
  ]

airwatch-app-activity = {
    Vendor = VMware
    Product = VMware AirWatch
    TimeFormat = "MMMM dd, yyyy HH:mm:ss"
    Fields = [
      """Timestamp: ({time}\w+\s\d{1,2},\s\d{4}\s(\d{2}:){2}\d{2})""",
      """Event Type:\s*({event_name}[^=]+?)\s*User:""",
      """User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s*Event Source:"""
      """"Application=({app}[^;=]+);\w+="""
    ]
     DupFields = ["event_name->opration"
}
```