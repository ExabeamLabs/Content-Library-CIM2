#### Parser Content
```Java
{
Name = proofpoint-tappod-leef-email-resolvestatus
Vendor = Proofpoint
Product = Proofpoint Email Protection
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
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
  """ ({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"ts"+:\s*"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """("|')ts("|')+:\s*("|')+({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+)""",
  """"host"+:\s*"+\[?({host}[\w\-.]+)\]?""""
  """"from"+:\s*"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
  """"rcpts"+:\s*\[({email_recipients}"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"*[^\]]*?)\]"""
  """"sizeBytes"+:\s*({bytes}\d+)"""
  """"filter":.+?disposition":"({result}[^"]+)""""
  """"ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"rule"+:\s*"+({rule}[^",]+)""""
  """"guid"*:\s*"*({message_id}[^"]+)""""
  """"routeDirection"+:\s*"+({direction}[^"]+)"""
  """"message-id"+:\s*\["+<*({message_id}[^>"]+)"""
  """"detectedName"+:\s*"+\s*({email_attachment}[^"]+)""""
  """"return-path"+:\s*\["+(<>|({return_path}[^"]+))""""
  """"detectedName"+:"+({attachment_1}[^"]+)"(.+?detectedName"+:"+({attachment_2}[^"]+)")?(.+?detectedName"+:"+({attachment_3}[^"]+)")?(.+?detectedName"+:"+({attachment_4}[^"]+)?")?(.+?detectedName"+:"+({attachment_5}[^"]+)")?(.+?detectedName"+:"+({attachment_6}[^"]+)")?(.+?detectedName"+:"+({attachment_7}[^"]+)")?(.+?detectedName"+:"+({attachment_8}[^"]+)")?(.+?detectedName"+:"+({attachment_9}[^"]+)")?(.+?detectedName"+:"+({attachment_10}[^"]+)")?"""
  """"cc"+:\[({cc}[^\]]+)\]"""
  """msgParts":[^\n]*?"detectedName":"[^",]*(\.({file_ext}\w+))""",
  """"spf":\{[^\}]*?result":"({spf_result}[^"]+)"""",
  """"dkimv":\[?\{[^\]\}]*?result":"({dkim_result}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```