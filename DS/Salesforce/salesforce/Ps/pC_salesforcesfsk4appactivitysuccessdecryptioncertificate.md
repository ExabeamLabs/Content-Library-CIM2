#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-decryptioncertificate"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """Action\=samlSsoConfig_decryptionCertificate;"""
  """Sales Cloud"""
]
Fields = [
  """CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
  """Action\\=({operation}[^;]+)"""
  """Display\\=({additional_info}.+?)\s*(\w+=|$)"""
  """Display\\=Changed ({resource}.+?) for ({object}.+?) from"""
  """({app}Sales Cloud)"""
]
ParserVersion = "v1.0.0"


}
```