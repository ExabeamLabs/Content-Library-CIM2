#### Parser Content
```Java
{
Name = mimecast-es-sk4-email-receive-impersonationprotect
    Vendor = Mimecast
    Product = Email Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """dproc=TTP Impersonation Protect""", """destinationServiceName =Mimecast Email Security""", """"senderAddress":""", """"recipientAddress":""" ]
    Fields = [
      """"eventTime":"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}(\+|-)\d+?)"""",
      """"senderAddress":"({email_address}[^",]+?)"""",
      """"recipientAddress":"({dest_email_address}[^",]+?)"""",
      """"senderIpAddress":"({src_ip}[^",]+?)"""",
      """"subject":"({email_subject}[^"]+?)"""",
      """"action":"({action}[^"]+?)"""",
      """"messageId":"({message_id}[^",]+?)"""",
      """"definition":"({additional_info}[^",]+?)"""",

    ]
	ParserVersion = "v1.0.0"


}
```