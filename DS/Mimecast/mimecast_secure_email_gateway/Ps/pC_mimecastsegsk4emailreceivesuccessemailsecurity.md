#### Parser Content
```Java
{
Name = "mimecast-seg-sk4-email-receive-success-emailsecurity"
Vendor = "Mimecast"
Product = "Mimecast Secure Email Gateway"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """destinationServiceName =Mimecast Email Security"""
  """"sender":""""
  """"recipient":""""
  """"msgid":""""
  """"reason":""""
  """"urlCategory":""""
]
Fields = [
  """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)""""
  """"sender":"({src_email_address}[^@"]+@[^\."]+\.[^"]+)""""
  """"recipient":"({dest_email_address}[^@"]+@[^\."]+\.[^"]+)""""
  """"subject":"({email_subject}[^"]+)""""
  """"route":"({direction}[^"]+)""""
   """"action":"({action}[^"]+)""""
  """"msgid":"<({message_id}[^"]+)>""""
  """"sourceIp":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"url":"({url}[^"]+)""""
  """"urlCategory":"({category}[^"]+)""""
  """"reason":"({reason}[^"]+)""""
  """"acc":"({user}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```