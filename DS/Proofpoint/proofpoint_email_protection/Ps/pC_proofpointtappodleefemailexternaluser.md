#### Parser Content
```Java
{
Name = proofpoint-tappod-leef-email-externaluser
Vendor = Proofpoint
Product = Proofpoint Email Protection
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
  """"subject""""
  """"from""""
  """"rcpts""""
  """"rule""""
  """"to""""
  """:"""
  """|Proofpoint|ProofpointEmailSecurity|"""
]
Fields = [
  """"timestamp"+:\s*"+({time}\d+.\d+-\d+T\d+:\d+:\d+.\d+Z)"""
  """"ts"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+)"""
  """"sizeBytes"+:\s*({bytes}\d+)"""
  """"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """"subject"+:\s*\["+({email_subject}[^"]+?)\s*""""
  """"rcpts"+:\s*\[({email_recipients}"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?"*)\]"""
  """"filter"+:.*?"disposition"+:\s*"+({result}[^"]+)"""
  """"routeDirection"+:\s*"+({direction}[^"]+)"""
  """"message-id"+:\s*\["+<*({message_id}[^>"]+)"""
  """msgParts.+"detectedName"+:\s*"+\s*({email_attachment}[^"]+)"""
  """msgParts"+:[^\n]*?"detectedName"+:"+[^",]*(\.({file_ext}\w+))"""
  """msgParts.+"sizeDecodedBytes":\s{0,99}({bytes}\d+)"""
  """"ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"x-originating-ip"+:\s*\["+\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"host"+:\s*"+\[?({host}[\w\-.]+)\]?""""
]
DupFields = [
  "email_attachment->email_attachments"
]
ParserVersion = "v1.0.0"


}
```