#### Parser Content
```Java
{
Name = microsoft-x-csv-email-send-success-routing
  ParserVersion = v1.0.0
  Conditions = [ 
""",ROUTING,DUPLICATEEXPAND,"""
""",Originating,""" 
]

exchange-dlp-email-alert-1 = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
     """Hostname=({host}[\w.\-]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({src_host}[\w\-\.]+)),(|::1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)),("[^"]*",|[^,]*,){6,7}(({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}([^;\]\s"\\,\|;]+\.[^;\]\s"\\,\|;]+)))(?<!local)(?<!loc)(?<!localdomain)(?<!internal))|[^,]*),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|({email_subject}[^,"]+?))\s*,(|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)(?<!localdomain))|[^,]*),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({src_host}[\w\-\.]+)),(|::1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)),("[^"]*",|[^,]*,){6,7}(({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}([^;\]\s"\\,\|;]+\.[^;\]\s"\\,\|;]+)))(?<!local)(?<!loc)(?<!localdomain)(?<!internal))|[^,]*),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|"\s*({email_subject}[^"]+?)\s*".*?)\s*,(|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),"""
     """,(SMTP|AGENT|ROUTING|DSN),[A-Z]+,([^,]*,){3}[\s<]*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,>]*?)(?<!local)(?<!loc)(?<!localdomain)(?<!internal)[\s>]*,"""
  
}
```