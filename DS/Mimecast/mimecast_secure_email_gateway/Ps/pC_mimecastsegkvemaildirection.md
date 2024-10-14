#### Parser Content
```Java
{
Name = mimecast-seg-kv-email-direction
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "epoch"
  Conditions = [ """|aggregateId=""", """|processingId=""", """|accountId=""", """|senderEnvelope=""", """|direction=""", """|rejectionInfo=""" ]
  Fields = [
    """\|timestamp=({time}\d{13})""",
    """\|host=({host}[\w\-.]+)\|""",
    """\|aggregateId=({alert_id}[^\|]+)\|""",
    """\|processingId=({process_id}[^\|]+)\|""",
    """\|(direction|route)=({direction}[^\|=]+)""",
    """\|act=({action}[^\|]+)\|""",
    """\|senderDomain=({src_domain}[^\|]+)\|""",
    """\|senderHeader=(<>|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
    """\|senderEnvelope=(|<>|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\|""",
    """\|recipients=(|<>|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\|""",
    """\|subject="({email_subject}[^"\|]+)"\|""",
    """\|source=({log_source}[^\|]+)\|""",
    """\|accountId=({account_id}[^\|]+)\|""",
    """\|messageId=({message_id}[^\|]+)\|""",
    """\|senderIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|""",
    """\|totalSizeAttachments=({attachment_size}\d+)""",
    """\|numberAttachments=({attachment_count}\d+)""",
    """\|attachments=(None|({email_attachment}[^\|,;]+))""",
    """\|attachments=(None|({email_attachments}[^\|]+))\|""",
    """\|rejectionType="*(None|({result_reason}[^\|]+?))"*"\|""",
    """\|rejectionCode=(None|({result_code}[^\|]+))\|""",
    """\|rejectionInfo="*(None|({result}[^\|]+?))"*\|"""
  ]
  ParserVersion = "v1.0.0"


}
```