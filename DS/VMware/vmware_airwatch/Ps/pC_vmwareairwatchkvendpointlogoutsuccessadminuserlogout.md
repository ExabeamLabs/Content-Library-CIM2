#### Parser Content
```Java
{
Name = vmware-airwatch-kv-endpoint-logout-success-adminuserlogout
  Vendor = VMware
  Product = VMware AirWatch
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
  Conditions = [ """AirWatch""", """Event Timestamp:""", """Event: AdminUserLoggedOut""" ]
  Fields = [
      """Timestamp: ({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,6})"""
      """Event Type:\s*({event_name}[^=]+?)\s*User:""",
      """User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*Event Source:"""
      """"Application=({app}[^;=]+);\w+="""
    ]
    DupFields = ["event_name->opration"]
    ParserVersion = "v1.0.0"


}
```