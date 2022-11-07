#### Parser Content
```Java
{
Name = microsoft-x-csv-email-send-success-mailboxrule
  ParserVersion = v1.0.0
  Conditions = [ 
""",MAILBOXRULE,RECEIVE,"""
""",Originating,""" 
]

exchange-dlp-email-alert-1 = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:m:ss.SSS"
  Fields = [
     """Hostname=({host}[\w.\-]+)""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}[a-fA-F\d.:]+)),(|({src_host}[^,]+)),(|::1|({dest_ip}[a-fA-F\d.:]+)),(|({dest_host}[^,]+)),("[^"]*",|[^,]*,){6,7}(|({email_recipients}({dest_email_address}[^,;@]+@[^,;@]+)[^,]*?)),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|({email_subject}[^,"]+?))\s*,(|({email_address}[^,@]+@[^,@]+)),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}[a-fA-F\d.:]+)),(|({src_host}[^,]+)),(|::1|({dest_ip}[a-fA-F\d.:]+)),(|({dest_host}[^,]+)),("[^"]*",|[^,]*,){6,7}(|({email_recipients}({dest_email_address}[^,;@]+@[^,;@]+)[^,]*?)),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|"\s*({email_subject}[^"]+?)\s*".*?)\s*,(|({email_address}[^,@]+@[^,@]+)),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),"""
  
}
```