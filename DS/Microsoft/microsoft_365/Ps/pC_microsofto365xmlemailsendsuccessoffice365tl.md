#### Parser Content
```Java
{
Name = "microsoft-o365-xml-email-send-success-office365-tl"
    Vendor = "Microsoft"
    Product = "Microsoft 365"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS"
    Conditions = [
      "office365"
      "<d:fromip"
      "<d:organization"
      "<d:subject"
      "messagetrace"
    ]
    Fields = [
      "(?i)<d:Received.+?>({time}.+?)<\\/d:Received>"
      "(?i)<d:SenderAddress>({src_email_address}.+?)<\\/d:SenderAddress>"
      "(?i)<d:RecipientAddress>({dest_email_address}.+?)<\\/d:RecipientAddress>"
      "(?i)<d:Subject>({email_subject}.+?)<\\/d:Subject>"
      "(?i)<d:Organization>({domain}.+?)<\\/d:Organization>"
      "(?i)<d:StartDate.+?>({time_started}.+?)<\\/d:StartDate>"
      "(?i)<d:EndDate.+?>({time_ended}.+?)<\\/d:EndDate>"
      "(?i)<d:FromIP>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?<\\/d:FromIP>"
      "(?i)<d:Size.+?>({bytes}\\d+)<\\/d:Size>"
      "(?i)<d:Status>({result}.+?)<\\/d:Status>"
    ]
    DupFields = [
      "email_subject->alert_name"
    ]
    ParserVersion = "v1.0.0"
  

}
```