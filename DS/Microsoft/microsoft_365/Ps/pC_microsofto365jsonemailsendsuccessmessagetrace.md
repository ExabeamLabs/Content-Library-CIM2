#### Parser Content
```Java
{
Name = microsoft-o365-json-email-send-success-messagetrace
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS"
  Conditions = [ """office365""", """"d:FromIP"""", """"d:Organization"""", """"d:Subject"""", """MessageTrace""" ]
  Fields = [
    """"d:Received":.+?#text":\s*"({time}[^"]+)"""", 
    """"d:SenderAddress":\s*"({src_email_address}[^"]+)"""",
    """"d:RecipientAddress":\s*"({dest_email_address}[^"]+)"""",
    """"d:Subject"":\s*"({email_subject}[^"]+)"""",
    """"d:Organization":\s*""({email_domain}[^"]+)"""",
    """"d:StartDate":.+?#text"":\s*"({time_started}[^"]+)"""",
    """"d:EndDate":.+?#text"":\s*"({time_ended}[^"]+)"""",
    """"d:FromIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"d:Size":.+?#text":\s*""({bytes}\d+)"""",
    """"d:Status":\s*"({result}[^"]+)"""",
  ]
  DupFields = [ "email_subject->alert_name" ]
  ParserVersion = "v1.0.0"


}
```