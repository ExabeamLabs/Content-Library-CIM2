#### Parser Content
```Java
{
Name = lastpass-l-sk4-app-login-success-adminconsole
  Vendor = LastPass
  Product = LastPass
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""""Data":""",  """Action":"Login to Admin Console""","""dproc=EventReporting""","""destinationServiceName =LastPass"""]
  Fields = [
    """"Time":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"IP_Address":"({src_ip}[a-fA-F\d:.]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+="""
    """"+Action"+:"+({event_name}[^"]+)"+""",
    """"Username"+:"+({email_address}[^@"]+@[^\."]+(\.[^"]+)?)""",
    """"+Data"+:"+({additional_info}[^"\}]+)"""
  ]
  ParserVersion = v1.0.0


}
```