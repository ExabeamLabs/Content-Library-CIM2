#### Parser Content
```Java
{
Name = vmware-airwatch-kv-endpoint-login-success-adminuserloggedin
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """AirWatch""", """Event Timestamp:""", """ConsoleEvent: AdminUserLoggedIn""" ]
  Fields = ${VMWareParsersTemplates.airwatch-app-activity.Fields}[
    """Timestamp: ({time}\w+\s\d{1,2}\s\d+:\d+:\d+)"""
    """({result}AdminUserLoggedIn)"""
  ]

airwatch-app-activity = {
    Vendor = VMware
    Product = VMware AirWatch
    TimeFormat = ["MMMM dd, yyyy HH:mm:ss","MMM dd HH:mm:ss"]
    Fields = [
      """Timestamp:\s*({time}\w+\s\d+\s(\d{2}:){2}\d{2})""",
      """Timestamp:\s*({time}\w+\s\d{1,2},\s\d{4}\s(\d{2}:){2}\d{2})""",
      """Event Type:\s*({operation}({event_name}[^=]+?))\s*User:""",
      """User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*Event Source:"""
      """"Application=({app}[^;=]+);\w+="""
    
}
```