#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-changedcommunitynickname"
Product = "Salesforce"
Conditions = [
"""Action\=changedcommunitynickname;"""
"""Sales Cloud"""
]
ParserVersion = "v1.0.0"

SSSZ"
    Fields = [
      """CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))""",
      """Action\\=({operation}[^;]+)""",
      """Display\\=({additional_info}.+?)\s*(\w+=|$)""",
      """({app}Sales Cloud)"""	  
    
}
```