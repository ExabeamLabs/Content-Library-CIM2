#### Parser Content
```Java
{
Name = "microsoft-o365-xml-email-send-success-office365"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS"
Conditions = [
  """office365"""
  """<d:FromIP"""
  """<d:Organization"""
  """<d:Subject"""
  """MessageTrace"""
]
Fields = [
  """<d:Received.+?>({time}.+?)<\/d:Received>"""
  """<d:SenderAddress>({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))<\/d:SenderAddress>"""
  """<d:RecipientAddress>({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))<\/d:RecipientAddress>"""
  """<d:Subject>({email_subject}.+?)<\/d:Subject>"""
  """<d:Organization>({domain}.+?)<\/d:Organization>"""
  """<d:StartDate.+?>({time_started}.+?)<\/d:StartDate>"""
  """<d:EndDate.+?>({time_ended}.+?)<\/d:EndDate>"""
  """<d:FromIP>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/d:FromIP>"""
  """<d:Size.+?>({bytes}\d+)<\/d:Size>"""
  """<d:Status>({result}.+?)<\/d:Status>"""
]
DupFields = [
  "email_subject->alert_name"
]
ParserVersion = "v1.0.0"


}
```