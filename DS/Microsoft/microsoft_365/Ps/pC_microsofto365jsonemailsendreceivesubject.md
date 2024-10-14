#### Parser Content
```Java
{
Name = microsoft-o365-json-email-send-receive-subject
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSS","yyyy-MM-dd'T'HH:mm:ss.SSSSSS","yyyy-MM-dd'T'HH:mm:ss.SSSSS","yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ 
    """"MessageTraceId":"""",
    """"SenderAddress":"""",
    """"RecipientAddress":"""",
    """"Subject":"""
  ]
  Fields = [
    """"StartDate":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """"StartDate":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"Date":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"Received":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?)""",
    """"Subject":"\s*({email_subject}.+?)\s*"}""",
    """"Subject":"\s*({email_subject}.+?)\s*",""",
    """"Direction":"({direction}[^"]+)"""",
    """"SenderAddress":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""",
    """"RecipientAddress":"({email_recipients}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""",
    """"RecipientAddress":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"Size":"?({bytes}\d+)""",
		""""VerdictSource":"({result}[^",]+)"""",
    """"Status":"({result}[^"]+)"""",
    """"ToIP":"?(?:null|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"FromIP":"?(?:null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"EventType":"({result_reason}[^"]+)"""",
    """"MessageTraceId":"({message_id}[^"]+)"""",
    """"MessageId":"({message_id}[^"]+)"""",
    """"triggered-by":\{"user-email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """Category\s+\[({category}[^\]]+)\]""",
    """"Action":"({action}[^",]+)"""",
    """"ToIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """dproc=({log_source}[^"\s]+)""", 
		""""MalwareName":"({malware_name}[^",]+)"""",

    """exa_json_path=$.StartDate,exa_field_name=time"""
    """exa_json_path=$.Date,exa_field_name=time"""
    """exa_json_path=$.Received,exa_field_name=time"""
    """exa_json_path=$.Subject,exa_field_name=email_subject"""
    """exa_json_path=$.Direction,exa_field_name=direction"""
    """exa_regex="SenderAddress":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""",
    """exa_regex="RecipientAddress":"({email_recipients}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""",
    """exa_regex="RecipientAddress":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.Size,exa_field_name=bytes"""
    """exa_json_path=$.VerdictSource,exa_field_name=result"""
    """exa_json_path=$.Status,exa_field_name=result"""
    """exa_regex="ToIP":"?(?:null|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """exa_regex="FromIP":"?(?:null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_json_path=$.EventType,exa_field_name=result_reason"""
    """exa_json_path=$.MessageTraceId,exa_field_name=message_id"""
    """exa_json_path=$.MessageId,exa_field_name=message_id"""
    """exa_regex="triggered-by":\{"user-email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """exa_json_path=$.Category,exa_field_name=category"""
    """exa_json_path=$.Action,exa_field_name=action"""
    """exa_regex="ToIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.MalwareName,exa_field_name=malware_name"""
  ]
 

}
```