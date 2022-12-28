#### Parser Content
```Java
{
Name = vmware-lastline-leef-app-notification-appliancestatus
  Vendor = VMware
  Product = Lastline
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss z"
  Conditions = [ """LEEF:""", """|Lastline|Enterprise|""", """deviceExternalId=""", """devTime=""", """|appliance-status|""" ]
  Fields = [
    """dvchost=({host}[\w\-.]+)""",
    """devTime=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+)""",
    """deviceStatusLink=({additional_info}.+?)\s+(\w+=|$)""",
    """cat=({operation}.+?)\s+(\w+=|$)""",
    """sev=({log_severity}.+?)\s+(\w+=|$)""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """msg=({event_name}.+?)\s+(\w+=|$)""",
    """deviceType=({operation_type}.+?)\s+(\w+=|$)""",
    """ApplianceName =({sensor_id}.+?)\s+(\w+=|$)""",
  ]


}
```