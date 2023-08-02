#### Parser Content
```Java
{
Name = zscaler-pa-json-app-login-success-signin
  ParserVersion = "v1.0.0"
  Conditions = [ """"AuditOperationType":"Sign In"""", """"User":"""", """"ObjectType":"Authentication"""" ]
  Fields = ${DLZscalerParsersTemplates.zscaler-audit-events.Fields} [
      """(\\)?"remoteIP\\":(\\)?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\\)?""""
  ]

zscaler-audit-events = {
    Vendor = Zscaler
    Product = Zscaler Private Access
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """"User":"(({email_address}[^"@]+@({email_domain}[^".]+\.[^"]+))|({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+))""",
      """"ObjectName":"({object}[^",]+)""",
      """"ObjectType":"({object_type}[^",]+)""",
      """"SessionID":"({session_id}[^"]+)""",
      """"AuditOperationType":"({event_name}[^"]+)""",
# customer_id is removed
      """"AuditNewValue":"({new_attribute}\{[^\}]+\})"""",
      """"AuditOldValue":"({old_attribute}\{[^\}]+\})""""
    
}
```