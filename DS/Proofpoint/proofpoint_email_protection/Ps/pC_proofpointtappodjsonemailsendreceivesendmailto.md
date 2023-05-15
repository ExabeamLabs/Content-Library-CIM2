#### Parser Content
```Java
{
Name = proofpoint-tappod-json-email-send-receive-sendmailto
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint Email Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
"""stat""",
""""cipher"""",
""""pps"""",
""""to"""",
""":"""
  ]
  Fields = [
    """"relay"+:\s*"+({host}[\w\-.]+?)\.?\s*\[({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"to"+:\s*\["+(\\u\d+)?({email_recipients}([^<@\]]+<|<|\\"+)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@([^\]\s"\\,\|>]+\.[^\]\s"\\,\|>]+)(?<!local))>?[^\]]*?)"+\]""",
    """"sizeBytes"+:\s*"*({bytes}\d+)""",
    """"ts"+:\s*"+({time}[^"]+)""",
    """"cipher"+:\s*"+(NONE|({auth_method}[^"]+))""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
    """"dsn"+:\s*"+({result}[^"]+)""",
    """"stat"+:\s*"+({action}(Sent|Deferred|User unknown|queued))""",
    """"return-path":\["(<>|({return_path}[^"]+))""""
  ]


}
```