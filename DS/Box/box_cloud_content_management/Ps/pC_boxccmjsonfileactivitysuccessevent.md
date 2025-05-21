#### Parser Content
```Java
{
Name = "box-ccm-json-file-activity-success-event"
Vendor = "Box"
Product = "Box Cloud Content Management"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "EEE MMM dd HH:mm:ss zzz yyyy"]
Conditions = [
   """created_by""""
   """created_at""""
    """event_id""""
    """event_type""""
]
Fields = [
    """\d+:\d+ ({host}[^\s]+) \{""",
    """[^\w]created_at":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d-\d\d:\d\d)""",
    """"created_at":"({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \w+ \d+)""""
    """[^\w]ip_address"+\s*:\s*"+(Unknown IP|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[",\]\}]""",
    """[^\w]event_type"+\s*:\s*"+({access}[^",]+)[",\]\}]""",
    """({app}Box|Okta)""",
    """[^\w]additional_details"+\s*:\s*[^\}]+[^\w]size"+\s*:\s*({bytes}\d+)[",\]\}]""",
    """[^\w]parent"\s*:\s*\{"type"\s*:\s*"folder,name"\s*:\s*"({folder_name}[^,]+),\w+"\s*:""",
    """[^\w]folder_name"+\s*:\s*"({folder_name}[^"]+)""",
    """[^\w]item_name"+\s*:\s*"+\s*({file_name}[^"]+?)[",\]\}]""",
    """[^\w]item_name"+\s*:\s*"+[^",]+?\.({file_ext}[^,\."]+),\w+":"""
    """[^\w]item_type"+\s*:\s*"+({file_type}[^",]+)[",\]\}]""",
    """[^\w]parent"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({file_dir}[^",]+)[",\]\}]""",
    """[^\w]additional_details"+\s*:\s*\{({additional_info}[^\}]+)[",\]\}]""",
    """[^\w]accessible_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+[^":,]*[",\]\}],"login":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+))"}""" ,
    """"role":"({access_type}[^"]+)"""",
    """filePermission=({permission}[^=]+?)\s+[\w]+="""
    """created_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({full_name}[^":,]+)[",\]\}]""",
    """created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
DupFields = [
  "access->operation"
  "host->dest_host"
  ]
ParserVersion = "v1.0.0"


}
```