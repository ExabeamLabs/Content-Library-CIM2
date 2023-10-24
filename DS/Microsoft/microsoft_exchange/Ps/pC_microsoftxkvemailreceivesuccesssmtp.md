#### Parser Content
```Java
{
Name = microsoft-x-kv-email-receive-success-smtp
  ParserVersion = v1.0.0
  Conditions = [ 
""",SMTP,SENDEXTERNAL,""" 
""",Incoming,""" 
]
 

exchange-dlp-email-alert-1 = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
     """Hostname=({host}[\w.\-]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({src_host}[^,]+)),(|::1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({dest_host}[^,]+)),("[^"]*",|[^,]*,){6,7}(({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}([^;\]\s"\\,\|;]+\.[^;\]\s"\\,\|;]+)))(?<!local)(?<!loc)(?<!localdomain)(?<!internal))|[^,]*),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|({email_subject}[^,"]+?))\s*,(|({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)(?<!localdomain))|[^,]*),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({src_host}[^,]+)),(|::1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({dest_host}[^,]+)),("[^"]*",|[^,]*,){6,7}(({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}([^;\]\s"\\,\|;]+\.[^;\]\s"\\,\|;]+)))(?<!local)(?<!loc)(?<!localdomain)(?<!internal))|[^,]*),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|"\s*({email_subject}[^"]+?)\s*".*?)\s*,(|({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),"""
     """,(SMTP|AGENT|ROUTING|DSN),[A-Z]+,([^,]*,){3}[\s<]*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,>]*?)(?<!local)(?<!loc)(?<!localdomain)(?<!internal)[\s>]*,"""
  
}
```