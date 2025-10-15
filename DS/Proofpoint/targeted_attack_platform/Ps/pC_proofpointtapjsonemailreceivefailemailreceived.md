#### Parser Content
```Java
{
Name = "proofpoint-tap-json-email-receive-fail-emailreceived"
Vendor = "Proofpoint"
Product = "Targeted Attack Platform"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
  """'subject':"""
  """'from':"""
  """'routeDirection':"""
  """'rcpts':"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[^:]+)\s"""
  """'startTime':\s*'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d+)"""
  """'sizeBytes':\s*({bytes}\d+)"""
  """'from':\s*\[?'[^@]*?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,\';\|]+))"""
  """'subject':\s*\['\s*({email_subject}.+?)\s*'"""
  """'envelope':\s*\{.*'rcpts':\s*\['({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\'\|]+)).*?)'\]"""
  """'ip':\s*'({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """'filter'.*?'action':\s*'({result}[^']+)'.*?'isFinal':\s*True"""
  """'filter'.*'isFinal':\s*True,\s*.*'action':\s*'({result}[^']+)'"""
  """'rule':\s*'({rule}[^']+)'"""
  """'isMsgReinjected':\s*({is_consolidated}\w+),"""
  """'connection':\s*\{.*'country':\s*'({country}[^']+)'"""
  """'appname':\s*'\s*({app}.+?)\s*'"""
  """'creator':\s*'\s*({creator}.+?)\s*'"""
  """'pagecount':\s*({page_count}\d+)"""
  """'folder':\s*'(?:({folder_name}[^']+))"""
  """'routeDirection':\s*'({direction}[^']+)"""
  """'message-id':\s*\['({message_id}[^']+)"""
  """'detectedName':\s*'({email_attachments}({email_attachment}[^']+))"""
  """'x-originating-ip':\s*\['\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """'host':\s*'\[?({host}[\w\-.]+)"""
  """eventTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
]
ParserVersion = "v1.0.0"


}
```