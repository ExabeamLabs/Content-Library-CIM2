#### Parser Content
```Java
{
Name = "proofpoint-tappod-json-email-receive-fail-emailreceived"
Vendor = "Proofpoint"
Product = "Proofpoint Email Protection"
ExtractionType = json
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
"""from":"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
"""subject":\["({email_subject}[^"]+?)\s*"\]"""
"""rcpts":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"[^\]]*)\]"""
"""filter":[^\n]*?"disposition":"({result}[^"]+)""""
"""routeDirection":"({direction}[^"]+)""""
""""message-id":\["<({message_id}[^">]+?)\s*>""""
"""msgParts":[^\n]*?"detectedName":"({email_attachment}[^"]+)""""
"""msgParts":[^\n]*?"sizeDecodedBytes":({bytes}\d+),"""
""""ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""host":"({host}[^"]+)""""
""""rule":"({rule}[^"]+)""""
"""fromDisplayNames":\["({full_name}[^"]+)""""
""""return-path":\["(<>|({return_path}[^"]+))""""
"""exa_regex="timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""
"""exa_json_path=$.msg.sizeBytes,exa_field_name=bytes""",
"""exa_regex=from":"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
"""exa_regex=subject":\["({email_subject}[^"]+?)\s*"\]"""
"""exa_regex=rcpts":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"[^\]]*)\]"""
"""exa_json_path=$.msg.header.subject[1:],exa_field_name=email_subject""",
"""exa_regex="subject"+:\s*\["+({email_subject}[^"]+)""",
"""exa_regex="ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""exa_json_path=$.connection.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.filter.disposition,exa_field_name=result""",
"""exa_json_path=$.filter.routeDirection,exa_field_name=direction""",
"""exa_regex="message-id":\["<({message_id}[^">]+?)\s*>"""",
"""exa_regex=msgParts":[^\n]*?"detectedName":"({email_attachment}[^"]+)""""
"""exa_json_path=$.msgParts[1:].sizeDecodedBytes,exa_regex=({bytes}\d+),""",
"""exa_regex=msgParts":[^\n]*?"sizeDecodedBytes":({bytes}\d+),"""
"""exa_json_path=$.connection.host,exa_field_name=host""",
"""exa_json_path=$.filter.quarantine.rule,exa_field_name=rule""",
"""exa_regex=fromDisplayNames":\["({full_name}[^"]+)""""
"""exa_regex="return-path":\["(<>|({return_path}[^"]+))""""
]
DupFields = [
  "email_attachment->email_attachments"
]
ParserVersion = "v1.0.0"


}
```