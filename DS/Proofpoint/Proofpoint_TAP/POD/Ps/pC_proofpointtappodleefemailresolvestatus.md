#### Parser Content
```Java
{
Name = proofpoint-tappod-leef-email-resolvestatus
Vendor = Proofpoint
Product = Proofpoint TAP/POD
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
  """"from"+:\s*"+({email_address}[^"@]+@[^"@]+)""""
  """"rcpts"+:\s*\[({email_recipients}"+({dest_email_address}[^"@]+@[^"]+)"*[^\]]*?)\]"""
  """"sizeBytes"+:\s*({bytes}\d+)"""
  """"filter"+:[^=]+?"+disposition"+:\s*"+({result}[^"]+)"""
  """"ip"+:\s*"+({src_ip}[a-fA-F\d.:]+)"""
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