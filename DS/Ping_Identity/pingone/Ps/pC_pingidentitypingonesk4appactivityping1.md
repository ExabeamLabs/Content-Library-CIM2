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
    """end=({time}\d{13})""",
    """cat=({category}[^\s]+)""",
    """IP\sAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Requested\sApplication\sID:\s*({requested_app_id}.*?)(\\n)*\s*Requested\sApplication\sName""",
    """Requested\sApplication\sName:\s*(N\/A|({requested_app}.*?))(\\n)*\s*Password\sReset""",
    """request=({action}[^\s]+)""",
    """requestClientApplication=({app}.*?)\s\w+=""",
    """suid=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=""",
    """suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=""",
   """flexString2=({action}.*?)\s\w*(:|=|")""",
    """Country:\s({country}.*?)\s*(\\n)*New Device""",
    """Mobile OS Version:\s({os}.*?)\s*(\\n)*Device Model""",
    """Device Model:\s(N\/A|({device_name}.*?))\s*(\\n)*Device Lock""",
    """"actors":\[\{"type":"user","name":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """dproc=({process_name}[^\s]+)"""
    """flexString2=({result}[^\s]+)"""
  ]


}
```