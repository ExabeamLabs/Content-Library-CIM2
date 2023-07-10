#### Parser Content
```Java
{
Name = onewelcome-ocip-json-app-authentication-fail-111405
  Conditions = [ """"originator":"onewelcome"""", """"siemcode":"111405"""", """"peptype":"AUTH-RES"""", """"pepmod":"emailsoauth"""" ]
  ParserVersion = v1.0.0

onewelcome-authentication-event = {
    Vendor = OneWelcome
    Product = OneWelcome Cloud Identity Platform
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
      """"account":"(?:-|({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"@]+?)(@({domain}[^"]+))?)"""",
      """"clientip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"siemcode":"({event_code}\d+)"""",
      """"useragent":"({user_agent}[^"]+)"""",
      """"app":"({app}[^"]+)"""",
      """"type":"({auth_type}[^"]+)"""",
      """"pepmod":"({object}[^"]+)"""",
      """"result":"({result}[^"]+)"""",
      """"authres":"({result}[^"]+)"""",
      """"action":"({event_name}[^"]+)"""",
      """"hdetail":"({additional_info}[^"]+)"""",
      """"human":"({additional_info}[^"]+)"""",
    ]
    DupFields = [ "event_name->operation" 
}
```