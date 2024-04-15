#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-file-download-success-group"
Product = "Microsoft 365"
Conditions = [
""""activityType":"Group""""
""""activityOperationType":"Assign""""
""""targetResourceType":""""
"""act="""
]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity.Fields} [
    """duser=((\w{1,5}:\w{1,5}:[^\#]*?)({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(Unknown|({user_sid}[^"\s\.]+))))"""
  
}
```