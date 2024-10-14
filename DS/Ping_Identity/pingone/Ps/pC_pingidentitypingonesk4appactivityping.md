#### Parser Content
```Java
{
Name = pingidentity-pingone-sk4-app-activity-ping
  ParserVersion = v1.0.0
  Vendor = Ping Identity
  Product = PingOne
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Ping"""]
  Fields = [
    """cat=({category}[^\s]+)""",
    """end=({time}\d{13})""",
    """dproc=({process_name}[^\s]+)"""
    """flexString2=({result}[^\s]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """suid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """oldFile=({user_agent}.*?)\s\w+=""",
    """msg=({additional_info}.*?)\s\w+=""",
    """fname=({full_name}.*?)\s\w+="""
  ]


}
```