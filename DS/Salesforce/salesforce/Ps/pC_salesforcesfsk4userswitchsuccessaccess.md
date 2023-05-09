#### Parser Content
```Java
{
Name = salesforce-sf-sk4-user-switch-success-access
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """destinationServiceName =Sales Cloud""", """cat=access""", """msg=""" ]
  Fields = [
  """CreatedDate\\?=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """Action\\?=({operation}[^;]+)""",
  """flexString2=({event_name}[^=]+)\s\w+="""
  """CreatedBy.Email\\?=({email_address}[^;@\s]+@[^\s;]+)"""
  """CreatedBy.Name\\?=({user}[^;]+)"""
  """suser=({account_name}[^\s]+)\s"""
  """({app}Sales Cloud)""",
  """Display\\?=({additional_info}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```