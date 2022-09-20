#### Parser Content
```Java
{
Name = citrix-cvapps-json-app-logout-success-applicationstop
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Virtual Apps
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event":"application-stop"""", """"system":"Citrix-XenApp"""", """"clientname":"""", """"servername":"""" ]
  Fields = [
    """"enddate":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"username":"(({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\+)?({user}[^"]+))"""",
    """({event_name}application-stop)""",
    """"servername":"({host}[^"]+)"""",
    """"clientaddress":"(0.0.0.0|({src_ip}[a-fA-F:\d.]+))"""",
    """"clientname":"({src_host}[^"]+)"""",
    """"clientplatform":"({os}[^"]+)"""",
    """"connectedviaipaddress":"({src_translated_ip}[a-fA-F:\d.]+)"""",
    """"application":"({app}[^"]+)""""
  ]


}
```