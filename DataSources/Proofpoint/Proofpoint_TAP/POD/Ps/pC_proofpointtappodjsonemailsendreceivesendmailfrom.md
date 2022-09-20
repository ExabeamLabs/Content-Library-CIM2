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
    """"relay"+:\s*"+({host}[\w\-.]+?)\.?\s*\[({dest_ip}[a-fA-F:\d.]+)""",
    """"from"+:\s*\[?"+([^<,]+?<|<)?({email_address}[^@>,]+@[^"\s\>,;]+)>?\s*"+\]?\}*?,""",
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