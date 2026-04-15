#### Parser Content
```Java
{
Name = microsoft-x-csv-email-failed
  ParserVersion = v1.0.0
  Conditions = [ 
""","Failed",""" 
]

exchange-dlp-email-alert} {
  Name = microsoft-x-csv-email-failed
  ParserVersion = v1.0.0
  Conditions = [ 
""","Failed",""" 
exchange-dlp-email-alert = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = ["yyyy/MM/dd H:mm:ss", "MM/dd/yyyy HH:mm:ss"]
  Fields = [
     """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d)"""
     """^.*?\s+({host}[\w.\-]+)\s+"<""",
     """({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+) (am|AM|pm|PM)","(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|[^"]*)","(.+?(recipients_cn=))?(({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)|[^"]*)",(|""|"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"),(|""|"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"),(|""|"({email_subject}.+?)\s*"),"({result}Delivered|Expanded|Failed|Resolved|FilteredAsSpam|Quarantined)",(""|"({bytes}\d+)")(,|\s*$|")""",
     """({host}[\w\-.]+)",([^,]*,){4}"*({time}\d\d\d\d\/\d\d\/\d\d\s+\d{1,2}:\d\d:\d\d)"*,"*(<>|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"*,"*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)"*,"*(|({email_subject}.+?))\s*"*,"*({result}Delivered|Expanded|Failed)"*,"*(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"*,"*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"*,"*({bytes}\d+)"""
  ]
}
}
```