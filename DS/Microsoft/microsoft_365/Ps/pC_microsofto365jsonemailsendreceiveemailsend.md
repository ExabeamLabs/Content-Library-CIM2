#### Parser Content
```Java
{
Name = microsoft-o365-json-email-send-receive-emailsend
ExtractionType = json
Vendor = Microsoft
Product = Microsoft 365
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS"]
Conditions = [
  """"RecipientAddress""""
  """"SenderAddress""""
  """"MessageTraceId""""
  """"Subject": """
]
Fields = [
  """exa_json_path=$.Received,exa_field_name=time"""
  """exa_json_path=$.DateReceived,exa_field_name=time"""
  """exa_json_path=$.RecipientAddress,exa_field_name=email_recipients"""
  """exa_json_path=$.RecipientAddress,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.SenderAddress,exa_regex=(<>|\\+|({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
  """exa_json_path=$.MessageId,exa_field_name=message_id"""
  """exa_json_path=$.ToIP,exa_regex=(?:null|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """exa_json_path=$.FromIP,exa_regex=(?:null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """exa_json_path=$.Subject,exa_field_name=email_subject"""
  """exa_json_path=$.Size,exa_field_name=bytes"""
  """exa_json_path=$.Status,exa_field_name=result"""
  """exa_json_path=$.Organization,exa_field_name=host"""
  """exa_json_path=$.MessageTraceId,exa_field_name=message_id"""
]
ParserVersion = "v1.0.0"


}
```