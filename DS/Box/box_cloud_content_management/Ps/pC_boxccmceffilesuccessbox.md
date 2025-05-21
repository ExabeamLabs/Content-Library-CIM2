#### Parser Content
```Java
{
Name = "box-ccm-cef-file-success-box"
Vendor = "Box"
Product = "Box Cloud Content Management"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "EEE MMM dd HH:mm:ss zzz yyyy"]
Conditions = [
"""destinationServiceName =Box"""
""""item_type":""""
""""item_name":""""
]
Fields = [
""""+created_at"+:"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d([\+\-]\d\d:\d\d)?)"""
""""created_at":"({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \w+ \d+)""""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
"""\ssuser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
""""item_name":"({file_name}[^"]+)""""
""""item_name":"([^\.]+?|(({file_name}[^"]+?(\.(|({file_ext}[^\.\s"]+?)))?)))",""""
""""item_type":"({file_type}[^"]+)"""
"""\sfname=({file_name}.+?)\s+(\w+=|$)"""
""""parent":\{[^\}]*?"name":"({file_dir}[^"]+)"""
""""file_path":"({file_dir}[^"]+)""""
""""event_type":"({access}[^"]+)"""
"""additional_details":\{[^\}]*?"size":({bytes}\d+)"""
"""(\||\s)requestClientApplication=({app}[^=]+?)(\s+\w+=|\s*$)"""
""""service_name":"({service_name}[^"]+)"""
""""shared_link_id":"({resource}[^,"\s]+?)""""
"""\smsg=({additional_info}.*?)\s\w+="""
"""owned_by"+:.+?"login"+:"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
""""user":\{[^\}]+?"name":"({full_name}[^"]+)","email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
"""created_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+({full_name}[^":,]+)[",\]\}]""",
"""created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|anonymous|Unknown User|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
DupFields = [
    "file_name->src_file_name"
    "file_ext->src_file_ext"
  ]
ParserVersion = "v1.0.0"


}
```