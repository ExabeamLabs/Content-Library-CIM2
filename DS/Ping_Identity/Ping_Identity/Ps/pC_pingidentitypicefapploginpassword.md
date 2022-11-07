#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-login-password
  Conditions = [ """CEF:""", """destinationServiceName =ping""", """"action":{"type":"Password"}""" ]
  ParserVersion = "v1.0.0"

cef-ping-events-skyformation = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "epoch"
  Fields = [
    """end=({time}\d+)""", 
    """cat=(N\/A|({category}[^\s]+))""",
    """destinationServiceName =({app}[^\s]+)""",
    """suser=(anonymous|({email_address}[^\s]+))""",
    """"ipAddress":"({src_ip}[A-Fa-f:\d.]+)"""",
    """"source":"({alert_name}[^"]+)"""",
    """"action"*:\{"*type"*:"*({event_name}[^"}]+)"""",
    """"result"*:\{"*status"*:"*({result}[^",]+)""",
    """"message"*:"*({event_name}[^"]+)"""",
    """"idpEntityId"*:"*({file_url}[^"]+)"""",
    """"client"*:\{"*id"*:"*({user_agent}[^"]+)"""",
    """msg=({additional_info}.+?)\soldFile=""",
  
}
```