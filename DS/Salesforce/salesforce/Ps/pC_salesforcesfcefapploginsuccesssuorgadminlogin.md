#### Parser Content
```Java
{
Name = "salesforce-sf-cef-app-login-success-suorgadminlogin"
  ParserVersion = "v1.0.0"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Action\=suOrgAdminLogin;""", """type\=SetupAuditTrail""", """Display\=""" ]
  Fields = [
    """CreatedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """({app}Sales Cloud)""",
    """cs1=({auth_method}[^\s]+)"""
    """CreatedBy\.Name\\?=({full_name}({first_name}[^\s]+)\s({last_name}[^;]+))""",
    """CreatedBy\.Username\\=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+));"""
    """Display\\=({additional_info}.+?)\s*(\w+=|$)"""
  ]


}
```