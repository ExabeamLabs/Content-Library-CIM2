#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-activity-adminauditlogs
  ParserVersion = v1.0.0
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """"type":"admin_audit_logs"""" , """destinationServiceName =Netskope""", """"data_values":""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""",
    """"category":"({additional_info}[^"]+)""",
    """"user":"(unknown|({email_address}[^@"\s]+@[^@"\s]+\.[^@"\s]+)?|(({domain}[^"@\\\/\s]+)[\\\/]+)?|({user}[^"\\\/\s]+))"""",
    """"audit_log_event":"({operation}[^"]+)""",
# data_values is removed
# supporting_data_type is removed
   ]


}
```