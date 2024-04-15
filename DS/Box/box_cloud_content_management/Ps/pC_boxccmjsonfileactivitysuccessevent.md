#### Parser Content
```Java
{
Name = "box-ccm-json-file-activity-success-event"
Vendor = "Box"
Product = "Box Cloud Content Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
   """created_by""""
   """created_at""""
    """event_id""""
    """event_type""""
]
Fields = [
    """\d+:\d+ ({host}[^\s]+) \{""",
    """[^\w]created_at":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d-\d\d:\d\d)""",
    """[^\w]ip_address"+\s*:\s*"+(Unknown IP|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[",\]\}]""",
    """[^\w]created_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({full_name}[^":]+)[",\]\}]""",
    """[^\w]created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(|({email_address}[^@"]+?@(([\.\w+]+\.)?({email_domain}[^\.\s"]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))|[^@"]+))|({user}[^"\s]+))[",\]\}]""",
    """[^\w]event_type"+\s*:\s*"+({access}[^",]+)[",\]\}]""",
    """({app}Box|Okta)""",
    """[^\w]additional_details"+\s*:\s*[^\}]+[^\w]size"+\s*:\s*({bytes}\d+)[",\]\}]""",
    """[^\w]folder_name"+\s*:\s*"+({bytes}\d+)[",\]\}]""",
    """[^\w]item_name"+\s*:\s*"+\s*({file_name}[^"]+?)[",\]\}]""",
    """[^\w]item_name"+\s*:\s*"+[^"]+?\.({file_ext}[^,\."]+)""""
    """[^\w]item_type"+\s*:\s*"+({file_type}[^",]+)[",\]\}]""",
    """[^\w]parent"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({file_dir}[^",]+)[",\]\}]""",
    """[^\w]additional_details"+\s*:\s*\{({additional_info}[^\}]+)[",\]\}]""",
    """[^\w]accessible_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+[^":,]*[",\]\}],"login":"({dest_user}[^":,]+?)"}""" ,
    """"role":"({access_type}[^"]+)"""",
]
DupFields = [
  "email_address->user"
  "access->operation"
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```