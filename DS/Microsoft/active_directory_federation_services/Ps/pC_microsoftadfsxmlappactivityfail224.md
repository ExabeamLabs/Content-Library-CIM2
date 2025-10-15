#### Parser Content
```Java
{
Name = microsoft-adfs-xml-app-activity-fail-224
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>224</EventID>""", """<Provider Name ="AD FS""""  ]
  Fields = [
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<TimeCreated SystemTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,9}Z)"\/>"""",
    """<Computer>({host}[\w\-\.]+)<\/Computer>""",
    """<EventData><Data>({additional_info}[^\<]+)<\/Data><\/EventData><\/Event>""",
    """thumbprint\s?'({new_hash}[^']+)"""
  ]
  ParserVersion = "v1.0.0"


}
```