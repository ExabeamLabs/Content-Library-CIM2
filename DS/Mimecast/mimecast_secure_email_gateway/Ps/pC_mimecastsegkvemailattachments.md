#### Parser Content
```Java
{
Name = mimecast-seg-kv-email-attachments
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "epoch"
  Conditions = [ """|aggregateId=""", """|processingId=""", """|accountId=""", """|senderEnvelope=""", """|attachments=""" ]
  Fields = [
    """\|timestamp=({time}\d{13})""",
    """\|host=({host}[\w\-.]+)\|""",
    """\|aggregateId=({alert_id}[^\|]+)\|""",
    """\|processingId=({process_id}[^\|]+)\|""",
    """\|emailSize=({bytes}\d+)""",
    """\|totalSizeAttachments=({attachment_size}\d+)""",
    """\|numberAttachments=({attachment_count}\d+)""",
    """\|attachments=(None|({email_attachment}[^\|,;]+))""",
    """\|attachments=(None|({email_attachments}[^\|]+))\|""",
    """\|signature=(None|({event_name}[^\|]+))\|"""
  ]
  ParserVersion = "v1.0.0"


}
```