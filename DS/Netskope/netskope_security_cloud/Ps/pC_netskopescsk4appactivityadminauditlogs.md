#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-activity-adminauditlogs
  ParserVersion = v1.0.0
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """"type":""", """"admin_audit_logs"""", """destinationServiceName =Netskope""", """"data_values":""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""",
    """"category":\s*"({additional_info}[^"]+)""",
    """"user":\s*"(unknown|({email_address}[^@"\s]+@[^@"\s]+\.[^@"\s]+)?|(({domain}[^"@\\\/\s]+)[\\\/]+)?|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"audit_log_event":\s*"({operation}[^"]+)""",
# data_values is removed
# supporting_data_type is removed
   ]


}
```