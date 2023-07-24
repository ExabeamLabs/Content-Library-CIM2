#### Parser Content
```Java
{
Name = armis-a-json-app-notification-success
  ParserVersion = v1.0.0
  Vendor = Armis
  Product = Armis Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"category":""", """"biosType":""", """"name":""", """"lastSeen":""", """"manufacturer":""" ]
  Fields = [
    """"category":"({device_type}[^"]+)""",
    """"id":(|({device_id}\d+)),""",
    """"ipv6":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""", 
    """"macAddress":"({src_mac}[^",]+)""",
    """"manufacturer":"({manufacturer}[^"]+)""", 
    """"operatingSystem":"({os}[^"]+)""",
    """"location":"({region}[^"]+)""",
    """"model":"({device_name}[^"]+)"""", 
  ] 


}
```