#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-salescloud"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """Action\=passwordexpiryForProfile;"""
  """Sales Cloud"""
]
Fields = [
  """CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
  """Action\\=({operation}[^;]+)"""
  """Display\\=({additional_info}.+?)\s*(\w+=|$)"""
  """Display\\=Changed profile ({object}.+?): Changed ({resource}.+?) from """
  """({app}Sales Cloud)"""
]
ParserVersion = "v1.0.0"


}
```