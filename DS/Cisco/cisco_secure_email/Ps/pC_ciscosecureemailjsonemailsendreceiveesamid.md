#### Parser Content
```Java
{
Name = cisco-secureemail-json-email-send-receive-esamid
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Secure Email
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  ExtractionType = json
  Conditions = [ """"ESAMID":"""", """"deviceExternalId":"""" ]
  Fields = [
    """exa_json_path=$.endTime,exa_field_name=time""",
    """exa_json_path=$.startTime,exa_field_name=time""",
    """exa_json_path=$.ESAMID,exa_field_name=alert_id""",
    """exa_json_path=$.ESAFriendlyFrom,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.suser,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.ESAReplyTo,exa_regex=^({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.duser,exa_regex=^({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.ESAStatus,exa_field_name=action""",
    """exa_json_path=$.act,exa_field_name=action""",
    """exa_json_path=$.ESAMsgSize,exa_field_name=bytes""",
    """exa_json_path=$.ESAAttachmentDetails,exa_regex='({email_attachment}[^'"]*(\.({file_ext}[^"']+)))""",
    """exa_json_path=$.deviceDirection,exa_field_name=direction""",
    """exa_json_path=$.cs4,exa_field_name=message_id""",
    """exa_json_path=$.sourceHostName,exa_regex=^({src_host}[\w\-.]+)$""",
    """exa_json_path=$.sourceAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.msg,exa_field_name=email_subject""",
    """exa_json_path=$.cs1,exa_field_name=policy_name"""
  ]


}
```