#### Parser Content
```Java
{
Name = proofpoint-tap-json-email-envelope
Vendor = Proofpoint
Product = Targeted Attack Platform
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """"from""""
  """"rcpts""""
  """"envelope""""
  """"pps""""
  """:"""
]
Fields = [
  """exa_json_path=$.ts,exa_field_name=time""",
  """exa_json_path=$.msg.sizeBytes,exa_field_name=bytes""",
  """exa_json_path=$.envelope.from,exa_regex=({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  """exa_regex="subject"+:\s*\["+({email_subject}[^"]+)"""
  """exa_regex="rcpts"+:\s*\[({email_recipients}"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?)\]"""
  """exa_json_path=$.connection.ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_json_path=$.filter.disposition,exa_field_name=result""",
  """exa_regex="routeDirection"+:\s*"+({direction}[^"]+)"""
  """exa_regex="message-id"+:\s*\["+({message_id}[^"]+)"""
  """exa_json_path=$.msgParts.detectedName,exa_field_name=email_attachment""",
  """exa_json_path=$.msgParts.sizeDecodedBytes,exa_field_name=bytes""",
  """exa_json_path=$.connection.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_regex="x-originating-ip"+:\s*\["+\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.connection.host,exa_field_name=host"""
]
DupFields = [
  "email_attachment->email_attachments"
]
ParserVersion = "v1.0.0"


}
```