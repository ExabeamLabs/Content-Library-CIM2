#### Parser Content
```Java
{
Name = "box-ccm-cef-file-success-move"
  Vendor = "Box"
  Product = "Box Cloud Content Management"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """"event_type":"MOVE""""
    """"type":"event""""
  ]
  Fields = [
    """"created_at":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"source":.*?"item_name":"({file_name}[^"]+\.({file_ext}[^"]+|))""",
    """"source":.*?"item_type":"({file_type}[^",]+)""",
    """"login":"({user}[\w\.\-]{1,40}\$?)"""",
    """"login":"({email_address}[^\s",@]+@[^\s",@]+)""",
    """"event_type":"({access}[^",]+)""",
    """"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"parent":.*?"name":"({file_dir}[^",]+)""",
    """"service_name":"({process_name}[^",]+)""",
    """"size":({bytes}\d+)""",
    """({app}Box)""",
    """[^\w]created_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({full_name}[^":,]+)[",\]\}]""",
    """[^\w]created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+.*?@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))""",										  
    """owned_by"+:.+?"login"+:"+({dest_email_address}[^\s@"]+@[^\s@"]+)"""
  ]
  DupFields = [ "file_name->src_file_name" , "file_ext->src_file_ext"]
  ParserVersion = "v1.0.0"


}
```