#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-sk4-app-activity-managementgeneral
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Office 365""", """dproc=management-general""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """\srt=({time}\d{13})""",
    """"Operation":"({event_name}[^"]+)"""",
# team_guid is removed
# team_name is removed
    """"UserId":"({user_id}[^"]+)"""",
    """destinationServiceName =({service_name}.+?)\s+(\w+=|$)""",
# device_inbound_interface is removed
    """dproc=({dproc}.+?)\s+(\w+=|$)""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""",
    """suser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
  ]


}
```