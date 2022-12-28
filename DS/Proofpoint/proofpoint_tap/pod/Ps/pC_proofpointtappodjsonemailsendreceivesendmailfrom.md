#### Parser Content
```Java
{
Name = proofpoint-tappod-json-email-send-receive-sendmailfrom
  ParserVersion = v1.0.0
  Vendor = Proofpoint
  Product = Proofpoint TAP/POD
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
"""msgid""",
""""cipher"""",
""""pps"""",
""""from"""",
""":"""
  ]
  Fields = [
    """"relay"+:\s*"+({host}[\w\-.]+?)\.?\s*\[({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"from"+:\s*\[?"+([^<,]+?<|<)?(\\u\d+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]>\s"\\,\|]+\.[^\]>\s"\\,\|]+)>?""",
    """"sizeBytes"+:\s*"*({bytes}\d+)""",
    """"nrcpts"+:\s*"+({num_recipients}\d+)""",
    """"proto"+:\s*"+({protocol}[^"]+)""",
    """"msgid"+:\s*"+<?({message_id}[^>"]+)""",
    """"ts"+:\s*"+({time}[^"]+)""",
    """"cipher"+:\s*"+(NONE|({auth_method}[^"]+))""",
    """"qid"+:\s*"+({alert_id}[^"]+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```