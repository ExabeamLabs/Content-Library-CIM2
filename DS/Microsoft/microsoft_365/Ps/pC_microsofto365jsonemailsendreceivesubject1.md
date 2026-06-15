#### Parser Content
```Java
{
Name = microsoft-o365-json-email-send-receive-subject-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SS"
  Conditions = [ """"messageId":""", """"senderAddress":"""", """"recipientAddress":"""", """"subject":""", """"fromIP":""", """"toIP":""" ]
  Fields = [
    """exa_json_path=$.messageId,exa_field_name=message_id""",
    """exa_json_path=$.status,exa_field_name=result""",
    """exa_regex="receivedDateTime":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d)""",
    """exa_regex="recipientAddress":"({email_recipients}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""",
    """exa_regex="recipientAddress":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """exa_regex="senderAddress":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""",
    """exa_json_path=$.subject,exa_field_name=email_subject"""
    """exa_json_path=$.size,exa_field_name=bytes"""
    """exa_regex="fromIP":"?(?:null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """exa_regex="toIP":"?(?:null|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""""
  ]


}
```