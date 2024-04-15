#### Parser Content
```Java
{
Name = "proofpoint-tappod-json-email-receive-fail-emailreceived"
Vendor = "Proofpoint"
Product = "Proofpoint Email Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"subject""""
  """"from""""
  """"rcpts""""
  """"rule""""
  """"to""""
  """"message-id""""
  """sizeDecodedBytes"""
  """"url":"""
  """"helo":"""
  """"fromHashed":"""
]
Fields = [
  """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""
  """msgSizeBytes":({bytes}\d+),"""
  """from":"({src_email_address}[^"@]+@[^\."]+\.[^\]\s"]+)""""
  """subject":\["({email_subject}[^"]+?)\s*"\]"""
  """rcpts":\[({email_recipients}"({dest_email_address}[^"@]+@[^\."]+\.[^\]\s"]+)"[^\]]*)\]"""
  """filter":[^\n]*?"disposition":"({action}[^"]+)""""
  """routeDirection":"({direction}[^"]+)""""
  """"message-id":\["<({message_id}[^">]+?)\s*>""""
  """msgParts":[^\n]*?"detectedName":"({email_attachment}[^"]+)""""
  """msgParts":[^\n]*?"sizeDecodedBytes":({bytes}\d+),"""
  """"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"host":"({host}[^"]+)""""
  """"rule":"({rule}[^"]+)""""
  """fromDisplayNames":\["({full_name}[^"]+)""""
  """"return-path":\["(<>|({return_path}[^"]+))""""
]
DupFields = [
  "email_attachment->email_attachments"
]
ParserVersion = "v1.0.0"


}
```