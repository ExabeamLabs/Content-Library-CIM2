#### Parser Content
```Java
{
Name = proofpoint-tappod-json-email-send-receive-sendmailfrom
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
"""msgid""",
""""cipher"""",
""""pps"""",
""""from"""",
""":"""
  ]
  Fields = [
    """"relay"+:\s*"+({host}[\w\-.]+?)\.?\s*\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"from"+:\s*\[?"+([^<,]+?<|<)?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|\>]+\.[^\]\s"\\,;\|\>]+))\s*>?""",
    """"sizeBytes"+:\s*"*({bytes}\d+)""",
    """"nrcpts"+:\s*"+({num_recipients}\d+)""",
    """"proto"+:\s*"+({protocol}[^"]+)""",
    """"msgid"+:\s*"+<?({message_id}[^>"]+)""",
    """"ts"+:\s*"+({time}[^"]+)""",
    """"cipher"+:\s*"+(NONE|({auth_method}[^"]+))""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
    """"to":\["<({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local))\s*>"""
    """exa_json_path=$.sm.relay,exa_regex=({host}[\w\-.]+?)\.?\s*\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.sm.from,exa_regex=([^<,]+?<|<)?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|\>]+\.[^\]\s"\\,;\|\>]+))\s*>?""",
    """exa_json_path=$.sm.sizeBytes,exa_field_name=bytes""",
    """exa_json_path=$.sm.nrcpts,exa_field_name=num_recipients""",
    """exa_json_path=$.sm.proto,exa_field_name=protocol""",
    """exa_json_path=$.sm.msgid,exa_regex=<?({message_id}[^>"]+)""",
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.tls.cipher,exa_field_name=auth_method,exa_match_expr=!Contains($.tls.cipher,"NONE")""",
    """exa_json_path=$.sm.qid,exa_field_name=alert_id""",
    """exa_regex="to":\["<({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local))\s*>"""
  ]
  DupFields = [ "host->dest_host" ]


}
```