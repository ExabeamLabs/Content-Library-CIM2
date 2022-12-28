#### Parser Content
```Java
{
Name = microsoft-x-csv-email-failed
  ParserVersion = v1.0.0
  Conditions = [ 
""","Failed",""" 
]

exchange-dlp-email-alert-1 = {
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:m:ss.SSS"
  Fields = [
     """Hostname=({host}[\w.\-]+)""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({src_host}[^,]+)),(|::1|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({dest_host}[^,]+)),("[^"]*",|[^,]*,){6,7}(|({email_recipients}({dest_email_address}[^,;@]+@[^,;@]+)[^,]*?)),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|({email_subject}[^,"]+?))\s*,(|({email_address}[^,@]+@[^,@]+)),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({src_host}[^,]+)),(|::1|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({dest_host}[^,]+)),("[^"]*",|[^,]*,){6,7}(|({email_recipients}({dest_email_address}[^,;@]+@[^,;@]+)[^,]*?)),("[^"]*",|[^,]*,)(|({bytes}\d+)),(|({num_recipients}\d+)),([^,]*,){2}\s*(|"\s*({email_subject}[^"]+?)\s*".*?)\s*,(|({email_address}[^,@]+@[^,@]+)),("[^"]*",|[^,]*,){2}(|({direction}Originating|Incoming)),"""
  
}
```