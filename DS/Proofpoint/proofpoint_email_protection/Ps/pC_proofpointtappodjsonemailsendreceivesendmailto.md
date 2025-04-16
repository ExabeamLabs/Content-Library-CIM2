#### Parser Content
```Java
{
Name = proofpoint-tappod-json-email-send-receive-sendmailto
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
"""stat""",
""""cipher"""",
""""pps"""",
""""to"""",
""":"""
  ]
  Fields = [
    """"relay"+:\s*"+({host}[\w\-.]+?)\.?\s*\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"sizeBytes"+:\s*"*({bytes}\d+)""",
    """"ts"+:\s*"+({time}[^"]+)""",
    """"cipher"+:\s*"+(NONE|({auth_method}[^"]+))""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
    """"dsn"+:\s*"+({result}[^"]+)""",
    """"stat"+:\s*"+({action}(Sent|Deferred|User unknown|queued))""",
    """"return-path":\["(<>|({return_path}[^"]+))"""",
    """exa_json_path=$.sm.relay,exa_regex=({host}[\w\-.]+?)\.?\s*\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.sm.to[1:],exa_regex=(\\u\d+)?<(([^<@\]]+<|<|\\"+)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local)))\s*>"""
    """exa_regex="to":\s*\["?<({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))"""
    """exa_json_path=$.sm.sizeBytes,exa_field_name=bytes""",
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.tls.cipher,exa_field_name=auth_method,exa_match_expr=!Contains($.tls.cipher,"NONE")""",
    """exa_json_path=$.sm.qid,exa_field_name=alert_id""",
    """exa_json_path=$.sm.dsn,exa_field_name=result""",
    """exa_json_path=$.sm.stat,exa_regex=({action}(Sent|Deferred|User unknown|queued))""",
    """exa_regex="return-path":\["(<>|({return_path}[^"]+))""""
    """"to"+:\s*\["+(\\u\d+)?<(([^<@\]]+<|<|\\"+)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local)))\s*>"""
  ]


}
```