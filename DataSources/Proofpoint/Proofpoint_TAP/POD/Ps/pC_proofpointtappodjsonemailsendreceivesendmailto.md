#### Parser Content
```Java
{
Name = proofpoint-tappod-json-email-send-receive-sendmailto
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint TAP/POD
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
"""stat""",
""""cipher"""",
""""pps"""",
""""to"""",
""":"""
  ]
  Fields = [
    """"relay"+:\s*"+({host}[\w\-.]+?)\.?\s*\[({dest_ip}[a-fA-F:\d.]+)""",
    """"to"+:\s*\["+({email_recipients}([^<@\]]+<|<|\\"+)?({dest_email_address}[^@\]]+@[^\\\s\>;,"]+)>?[^\]]*?)"+\]""",
    """"sizeBytes"+:\s*"*({bytes}\d+)""",
    """"ts"+:\s*"+({time}[^"]+)""",
    """"cipher"+:\s*"+(NONE|({auth_method}[^"]+))""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
    """"dsn"+:\s*"+({result}[^"]+)""",
    """"stat"+:\s*"+({action}(Sent|Deferred|User unknown|queued))""",
    """"return-path":\["(<>|({return_path}[^"]+))""""
  ]
  DupFields = ["host->dest_host"]


}
```