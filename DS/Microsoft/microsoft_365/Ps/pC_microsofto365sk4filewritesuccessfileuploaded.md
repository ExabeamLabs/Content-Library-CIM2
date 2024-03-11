#### Parser Content
```Java
{
Name = microsoft-o365-sk4-file-write-success-fileuploaded
Product = "Microsoft 365"
Conditions = [
  """"Operation":"FileUploaded""""
  """"Workload":""""
  """"SourceFileName":""""
]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity.Fields} [
    """duser=((\w{1,5}:\w{1,5}:[^\#]*?)({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(Unknown|({user_sid}[^"\s\.]+))))"""
  
}
```