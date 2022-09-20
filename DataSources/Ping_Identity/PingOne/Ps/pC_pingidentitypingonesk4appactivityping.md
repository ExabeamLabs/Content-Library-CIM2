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
    """end=({time}\d+)""",
    """dproc=({process_name}[^\s]+)"""
    """flexString2=({result}[^\s]+)""",
    """src=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
    """suid=({user}[^\s]+)""",
    """suser=({user}[^\s]+)""",
    """oldFile=({user_agent}.*?)\s\w+=""",
    """msg=({additional_info}.*?)\s\w+=""",
    """fname=({full_name}.*?)\s\w+="""
  ]


}
```