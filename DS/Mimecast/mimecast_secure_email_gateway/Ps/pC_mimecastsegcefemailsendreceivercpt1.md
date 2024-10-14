#### Parser Content
```Java
{
Name = mimecast-seg-cef-email-send-receive-rcpt-1
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
      """"acc":"""
      """"MsgId":"""
      """"Sender":""""
      """"Route":"""
      """"Recipient":"""
	]
  Fields = [
      """destinationServiceName =({app}[^=]+)\s\w+="""
      """dproc=({dproc}[^=]+)\s\w+="""
      """\srequestMethod=(?:-|({method}[^=]+?))\s\w+="""
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """"(Source)?IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s"""
      """"RejType":"({outcome_type}[^"]+)"""
      """"Err(or)?":"({failure_reason}[^"]+)"""
      """suid=({suid}[^\s]+)\s+\w+="""
      """"acc":"({host}[^",]+)"""",
      """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
      """"Act":"({action}[^"]+)""",
      """request=({result}\S+)\s""",
      """"RejInfo":"({result}[^"]+)"""
      """"(Rcpt|Recipient)":"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)[^"]*)"""",
      """"Subject":"?(null|({email_subject}[^,"]+?))\s*"?,""",
      """Route":"({direction}[^"]+)"""
      """"aCode":"(|({alert_id}[^"]+?))"""",
      """"Sender":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
      """"MsgId":"?(null|({message_id}[^,"]+))\s*"?,"""
      """dtz=({dtz}[^\s]+)"""
      """"fileName":"({email_attachments}[^"]+)""""
      """"fileName":"({email_attachment}[^,"]*(\.({file_ext}[^",]+)))"""",
      """"sha256":"({hash_sha256}[^"]+)"""",
      """"Virus":"({alert_name}[^"]+)"""",
      """"fileMime":"({mime}[^"]+)"""",
      """"MsgId":\s*"<({message_id}[^"]+)>""""
  ]


}
```