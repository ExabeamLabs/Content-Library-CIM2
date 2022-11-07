#### Parser Content
```Java
{
Name = proofpoint-tap-json-email-envelope
Vendor = Proofpoint
Product = Proofpoint TAP
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """"from""""
  """"rcpts""""
  """"envelope""""
  """"pps""""
  """:"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[^:]+)\s"""
  """"ts"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+)"""
  """"sizeBytes"+:\s*({bytes}\d+)"""
  """"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}[^"@\s,<>]+@[^"@\s,<>]+)"""
  """"subject"+:\s*\["+({email_subject}[^"]+)"""
  """"rcpts"+:\s*\[({email_recipients}"+({dest_email_address}[^"@]+@[^"]+).*?)\]"""
  """"ip"+:\s*"+({dest_ip}[a-fA-F\d.:]+)"""
  """"filter"+:.*?"+disposition"+:\s*"+({result}[^"]+)"""
  """"routeDirection"+:\s*"+({direction}[^"]+)"""
  """"message-id"+:\s*\["+({message_id}[^"]+)"""
  """msgParts.+"detectedName"+:\s*"+\s*({email_attachment}[^"]+)"""
  """msgParts.+"sizeDecodedBytes":\s{0,99}({bytes}\d+)"""
  """"ip"+:\s*"+({src_ip}[A-Fa-f:\d.]+)"""
  """"x-originating-ip"+:\s*\["+\[({src_ip}[^"\]]+)"""
  """"host"+:\s*"+\[?({host}[\w\-.]+)\]?""""
]
DupFields = [
  "email_attachment->email_attachments"
]
ParserVersion = "v1.0.0"


}
```