#### Parser Content
```Java
{
Name = "mimecast-seg-kv-email-rcpt"
Vendor = "Mimecast"
Product = "Mimecast Secure Email Gateway"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
"""|Dir="""
"""|Sender="""
"""|Rcpt="""
]
Fields = [
  """datetime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\d\d[+-].+?)\|"""
  """datetime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\d\d)"""
  """\|aCode=(|({alert_id}[^\|]+?))\|"""
  """\|Route=(|({direction}[^\|]+?))\|"""
  """\|Dir=(|({direction}[^\|]+?))\|"""
  """\|Act=(|({action}[^\|]+?))\|"""
  """\|Delivered=(|({action}[^\|]+?))\|"""
  """\|RejType=\\(|({outcome_type}.+?))\\\|"""
  """\|Err=\\?(|({result}.+?))\\?\|"""
  """\|Error=\\?(|({result}.+?))\\?\|"""
  """\|RejInfo=\\?(|({result}.+?))\\?\|"""
  """\|Sender=(|<>|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\|"""
  """\|headerFrom=(|<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\|"""
  """\|Recipient=(|<>|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\|"""
  """\|Rcpt=(|<>|({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\|"""
  """\|Subject=\\?(|({email_subject}[^\|$]+?))\s*(\||$)"""
  """\|Snt=({bytes}\d+)\|"""
  """\|SpamScore=({spam_score}\d+)"""
  """\|SourceIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|IP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """AttCnt=\s*({attachment_count}\d+)"""
  """\|MsgId=<?({message_id}[^>\|]+)(>|\|)"""
]
ParserVersion = "v1.0.0"


}
```