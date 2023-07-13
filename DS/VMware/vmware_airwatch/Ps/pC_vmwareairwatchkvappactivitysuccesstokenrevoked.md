#### Parser Content
```Java
{
Name = vmware-airwatch-kv-app-activity-success-tokenrevoked
  Conditions = [ """AirWatch""", """Event Timestamp:""", """DeviceEvent: AuthTokenRevoked""" ]
  ParserVersion = "v1.0.0"

airwatch-app-activity = {
    Vendor = VMware
    Product = VMware AirWatch
    TimeFormat = "MMMM dd, yyyy HH:mm:ss"
    Fields = [
      """Timestamp: ({time}\w+\s\d{1,2},\s\d{4}\s(\d{2}:){2}\d{2})""",
      """Event Type:\s*({event_name}[^=]+?)\s*User:""",
      """User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s*Event Source:"""
    ]
     DupFields = ["event_name->opration"
}
```