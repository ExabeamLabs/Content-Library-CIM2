#### Parser Content
```Java
{
Name = salesforce-sf-sk4-app-activity-success-addedtodelegatedgroup
Conditions = [
  """Action\=addedtodelegatedgroup;"""
  """Sales Cloud"""
]
Fields = ${SalesforceParsersTemplates.cef-salesforce-app-activity-1.Fields}[
  """Display\\=Added ({object}.+?) to .*?delegated group"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
]
DupFields = [
  "email_address->user"
]
ParserVersion = "v1.0.0"

cef-salesforce-app-activity-1 = {
    Vendor = Salesforce
    Product = Salesforce
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))""",
      """Action\\=({operation}[^;]+)""",
      """Display\\=({additional_info}.+?)\s*(\w+=|$)""",
      """({app}Sales Cloud)"""	  
    
}
```