#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-sk4-app-activity-managementgeneral
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """destinationServiceName =Office 365""", """dproc=management-general""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"Operation":"({event_name}[^"]+)"""",
# team_guid is removed
# team_name is removed
    """"UserId":"({user_id}[^"]+)"""",
    """destinationServiceName =({service_name}.+?)\s+(\w+=|$)""",
# device_inbound_interface is removed
    """dproc=({dproc}.+?)\s+(\w+=|$)""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""",
    """suser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)""",
  ]


}
```