#### Parser Content
```Java
{
Name = "proofpoint-tappod-sk4-email-receive-fail-emailreceived"
Vendor = "Proofpoint"
Product = "Proofpoint Email Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """CEF"""
  """cipher"""
  """"from""""
  """:"""
  """"to""""
  """"pps":"""
  """msgid"""
]
Fields = [
  """"ts"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+)"""
  """"sizeBytes"+:\s*({bytes}\d+)"""
  """"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({src_email_address}[^"@\s,<>]+@[^"@\s,<>]+)"""
  """"subject"+:\s*\["+({email_subject}[^"]+?)\s*""""
  """"rcpts"+:\s*\["+({email_recipients}({dest_email_address}[^"@]+@[^"]+)[^\]]*?)"*\]"""
  """"routeDirection"+:\s*"+({direction}[^"]+)"""
  """"msgid"+:\s*"+<?({message_id}[^>"]+)"""
  """"detectedName"+:\s*"+\s*({email_attachment}[^"]+)"+,"+md5"""
  """"ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"host"+:\s*"+\[?({host}[\w\-.]+)\]?""""
  """"rules"+:\[[^\]]*"+rule"+:"+({rule}[^"]+)""""
  """"filter"+:.*?"+disposition"+:\s*"+({action}[^"]+)"""
  """"return-path"+:\["+(<>|({return_path}[^"\],]+))"""
]
ParserVersion = "v1.0.0"


}
```