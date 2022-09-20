#### Parser Content
```Java
{
Name = pingidentity-pingone-sk4-app-activity-ping-1
  Vendor = Ping Identity
  Product = PingOne
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Ping""", """|audit-event|""" ]
  Fields = [
    """end=({time}\d+)""",
    """cat=({category}[^\s]+)""",
    """IP\sAddress:\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """Requested\sApplication\sID:\s*({requested_app_id}.*?)(\\n)*\s*Requested\sApplication\sName""",
    """Requested\sApplication\sName:\s*(N\/A|({requested_app}.*?))(\\n)*\s*Password\sReset""",
    """request=({action}[^\s]+)""",
    """requestClientApplication=({app}.*?)\s\w+=""",
    """suid=({user}[^\s]+)""",
    """suser=({user}[^\s]+)""",
   """flexString2=({action}.*?)\s\w*(:|=|")""",
    """Country:\s({country}.*?)\s*(\\n)*New Device""",
    """Mobile OS Version:\s({os}.*?)\s*(\\n)*Device Model""",
    """Device Model:\s(N\/A|({device_name}.*?))\s*(\\n)*Device Lock""",
  ]


}
```