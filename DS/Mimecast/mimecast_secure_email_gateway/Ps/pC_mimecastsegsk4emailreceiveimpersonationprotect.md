#### Parser Content
```Java
{
Name = mimecast-seg-sk4-email-receive-impersonationprotect
    Vendor = Mimecast
    Product = Mimecast Secure Email Gateway
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"impersonationResults":""", """"impersonationDomainSource":""", """"senderAddress":""", """"recipientAddress":""" ]
    Fields = [
      """"eventTime":"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}(\+|-)\d+?)"""",
      """"senderAddress":"({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """"recipientAddress":"({dest_email_address}[^",]+?)"""",
      """"senderIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"subject":"({email_subject}[^"]+?)"""",
      """"action":"({action}[^"]+?)"""",
      """"messageId":"({message_id}[^",]+?)"""",
      """"definition":"({additional_info}[^",]+?)"""",

    ]
	ParserVersion = "v1.0.0"


}
```