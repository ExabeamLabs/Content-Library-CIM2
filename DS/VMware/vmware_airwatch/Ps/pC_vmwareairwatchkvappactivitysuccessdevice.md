#### Parser Content
```Java
{
Name = vmware-airwatch-kv-app-activity-success-device
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
  Conditions = [ """AirWatch""", """Event Timestamp:""", """Event:""", """Event Category: Device""" ]
  Fields = ${VMWareParsersTemplates.airwatch-app-activity.Fields}[
    """Timestamp: ({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,6})"""
  ]
  ParserVersion = "v1.0.0"

airwatch-app-activity = {
    Vendor = VMware
    Product = VMware AirWatch
    TimeFormat = ["MMMM dd, yyyy HH:mm:ss","MMM dd HH:mm:ss"]
    Fields = [
      """Timestamp:\s*({time}\w+\s\d+\s(\d{2}:){2}\d{2})""",
      """Timestamp:\s*({time}\w+\s\d{1,2},\s\d{4}\s(\d{2}:){2}\d{2})""",
      """Event Type:\s*({event_name}[^=]+?)\s*User:""",
      """User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s*Event Source:"""
      """"Application=({app}[^;=]+);\w+="""
    ]
     DupFields = ["event_name->operation"
}
```