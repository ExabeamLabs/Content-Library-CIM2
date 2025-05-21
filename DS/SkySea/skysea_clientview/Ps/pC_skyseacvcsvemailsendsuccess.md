#### Parser Content
```Java
{
Name = skysea-cv-csv-email-send-success
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ 
""",メール,""" 
]
  Fields = [
    """({host}[\w\-.]+),\d+,({src_host}[\w\-.]+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,[^,]*,({user}[\w\.\-\!\#\^\~]{1,40}\$?),(|({full_name}[^,\(\（]+(\（[^\）,]+\）)?)[^,]*),({time}\d+\/\d+\/\d+ \d+:\d+:\d+),([^,]*,){4}\s*(|({email_subject}[^,]+?))\s*,([^,]*,){21}(({email_recipients}<?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))[^,]*)|[^,]*),(<?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))>?|[^,]*),\s*(|({email_attachments}[^,]+?\.({file_ext}[^,]+)))\s*,"""
  ]


}
```