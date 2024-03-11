#### Parser Content
```Java
{
Name = proofpoint-tappod-leef-email-resolvestatus
Vendor = Proofpoint
Product = Proofpoint Email Protection
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"from""""
  """"rcpts""""
  """"rule""""
  """"helo""""
  """"actions""""
  """"suborgs""""
  """"resolveStatus""""
]
Fields = [
  """"ts"+:\s*"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}[\+\-]\d{1,4})"""
  """"host"+:\s*"+\[?({host}[\w\-.]+)\]?""""
  """"from"+:\s*"+({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
  """"rcpts"+:\s*\[({email_recipients}"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"*[^\]]*?)\]"""
  """"sizeBytes"+:\s*({bytes}\d+)"""
  """"filter"+:[^=]+?"+disposition"+:\s*"+({result}[^"]+)"""
  """"ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"rule"+:\s*"+({rule}[^",]+)""""
  """"guid"*:\s*"*({message_id}[^"]+)""""
  """"routeDirection"+:\s*"+({direction}[^"]+)"""
  """"message-id"+:\s*\["+<*({message_id}[^>"]+)"""
  """"detectedName"+:\s*"+\s*({email_attachment}[^"]+)""""
  """"return-path"+:\s*\["+(<>|({return_path}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```