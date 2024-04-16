#### Parser Content
```Java
{
Name = hmail-hmailserver-json-app-activity-winhmailserver
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Vendor = hMail
  Product = hMailServer
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"log_type":"win_hmailserver"""" ]
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.host.name,exa_field_name=host""",
    """exa_json_path=$.fields.log_type,exa_field_name=event_category""",
    """exa_regex=(MAIL FROM):<({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>""",
    """exa_regex="message":".*?\\t\d+\\t({session_id}\d+)\\t.*?\\t\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\"\\t\\"(\w+):""",
    """exa_regex=(RCPT TO):<({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))>""",
    """exa_regex=(?:MAIL FROM|RCPT TO):<({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>""",
  ]


}
```