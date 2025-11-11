#### Parser Content
```Java
{
Name = "pingidentity-pi-cef-app-authentication-fail-failure-1"
Conditions = [
"""CEF:"""
"""|Ping Identity|PingFederate|"""
"""|STS|STS|"""
"""msg=failure"""
]
ParserVersion = "v1.0.0"

cef-ping-events-skyformation = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "epoch"
  Fields = [
    """end=({time}\d{13})""", 
    """cat=(N\/A|({category}[^\s]+))""",
    """destinationServiceName =({app}[^\s]+)""",
    """suser=(anonymous|({email_address}[^\s]+))""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"source":"({alert_name}[^"]+)"""",
    """"action"*:\{"*type"*:"*({event_name}[^"}]+)"""",
    """"result"*:\{"*status"*:"*({result}[^",]+)""",
    """"message"*:"*({event_name}[^"]+)"""",
    """"idpEntityId"*:"*({file_url}[^"]+)"""",
    """"client"*:\{"*id"*:"*({user_agent}[^"]+)"""",
    """msg=({additional_info}.+?)\soldFile=""",
  
}
```