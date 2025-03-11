#### Parser Content
```Java
{
Name = "box-ccm-cef-file-success-move"
  Vendor = "Box"
  Product = "Box Cloud Content Management"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "EEE MMM dd HH:mm:ss zzz yyyy"]
  Conditions = [
    """"event_type":"MOVE""""
    """"type":"event""""
  ]
  Fields = [
    """"created_at":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"created_at":"({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \w+ \d+)""""
    """"source":.*?"item_name":"({file_name}[^"]+?(\.({file_ext}[^"\s]+))?)"""",
    """"source":.*?"item_type":"({file_type}[^",]+)""",
    """"login":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"login":"({email_address}[^\s",@]+@[^\s",@]+)""",
    """"event_type":"({access}[^",]+)""",
    """"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"parent":.*?"name":"({file_dir}[^",]+)""",
    """"file_path":"({file_dir}[^"]+)"""",
    """"service_name":"({process_name}[^",]+)""",
    """"size":({bytes}\d+)""",
    """({app}Box)""",
    """created_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({full_name}[^":,]+)[",\]\}]""",
    """created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",										  
    """owned_by"+:.+?"login"+:"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]
  DupFields = [ "file_name->src_file_name" , "file_ext->src_file_ext"]
  ParserVersion = "v1.0.0"


}
```