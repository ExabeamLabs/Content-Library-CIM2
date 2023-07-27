#### Parser Content
```Java
{
Name = zscaler-pa-json-app-logout-success-signout
  ParserVersion = "v1.0.0"
  Conditions = [ """"AuditOperationType":"Sign Out"""", """"User":"""", """"ObjectType":"Authentication"""" ]

zscaler-audit-events = {
    Vendor = Zscaler
    Product = Zscaler Private Access
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """"User":"(({email_address}[^"@]+@({email_domain}[^".]+\.[^"]+))|({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+))"""",
      """"ObjectName":"({object}[^",]+)""",
      """"ObjectType":"({object_type}[^",]+)""",
      """"SessionID":"({session_id}[^"]+)""",
      """"AuditOperationType":"({event_name}[^"]+)""",
# customer_id is removed
      """"AuditNewValue":"({new_attribute}\{[^\}]+\})"""",
      """"AuditOldValue":"({old_attribute}\{[^\}]+\})""""
    
}
```