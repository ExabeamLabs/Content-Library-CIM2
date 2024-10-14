#### Parser Content
```Java
{
Name = mimecast-seg-sk4-email-receive-impersonationprotect
    Vendor = Mimecast
    Product = Mimecast Secure Email Gateway
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"impersonationResults":""", """"impersonationDomainSource":""", """"senderAddress":""", """"recipientAddress":""" ]
    Fields = [
      """"eventTime":\s*"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}(\+|-)\d+?)"""",
      """"senderAddress":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """"recipientAddress":\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
      """"senderIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"subject":\s*"({email_subject}[^"]+?)"""",
      """"action":\s*"({action}[^"]+?)"""",
      """"messageId":\s*"<({message_id}[^",]+?)>"""",
      """"definition":\s*"({additional_info}[^",]+?)"""",

    ]
	ParserVersion = "v1.0.0"


}
```