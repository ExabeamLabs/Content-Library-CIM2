#### Parser Content
```Java
{
Name = "mimecast-seg-kv-email-sender"
Vendor = "Mimecast"
Product = "Mimecast Secure Email Gateway"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""|aCode="""
"""|Sender="""
"""|Subject="""
"""|acc="""
"""|MsgId="""
]
Fields = [
  """datetime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\d\d[+-]\d+)\|"""
  """\|aCode=(|({alert_id}[^\|]+?))\|"""
  """\|Act=(|({action}[^\|]+?))\|"""
  """\|MsgId=<?({message_id}[^>\|]+)(>|\|)"""
  """\|Sender=(|<>|({src_email_address}\S+?@\S+?))\|"""
  """\|SourceIP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|Recipient=(|<>|({dest_email_address}[^\|]+))\|"""
  """\|Subject=\\?(|({email_subject}[^\|$]+?))\s*(\||$)"""
  """\|AttNames=({email_attachments}[^\|]+?),?\s*\|"""
  """\|Route=(|({direction}[^\|]+?))\|"""
  """AttCnt=({attachment_count}\d+)"""
  """MsgSize=({bytes}\d+)"""
]
ParserVersion = "v1.0.0"


}
```