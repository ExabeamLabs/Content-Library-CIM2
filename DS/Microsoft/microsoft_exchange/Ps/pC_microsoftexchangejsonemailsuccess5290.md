#### Parser Content
```Java
{
Name = microsoft-exchange-json-email-success-5290
Vendor = Microsoft
Product = Microsoft Exchange
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"run_id":"""
  """"sender_address":"""
  """"recipient_domain":"""
]
Fields = [
  """exa_json_path=$.date_time,exa_field_name=time""",
  """exa_json_path=$.recipient_address,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
  """exa_json_path=$.email_direction,exa_field_name=direction""",
  """exa_json_path=$.message_subject,exa_field_name=email_subject""",
  """exa_json_path=$.attachment_name,exa_field_name=email_attachment,exa_match_expr=!Contains(toLower($.attachment_name),"unknown")""",
  """exa_json_path=$.sender_address,exa_regex=(({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))""",
  """exa_json_path=$.total_bytes,exa_field_name=bytes""",
  """exa_json_path=$.email_event,exa_field_name=action""",
]
DupFields = [
  "src_email_address->email_address"
]
ParserVersion = "v1.0.0"


}
```