#### Parser Content
```Java
{
Name = "box-ccm-cef-file-success-box"
Vendor = "Box"
Product = "Box Cloud Content Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""destinationServiceName =Box"""
""""item_type":""""
""""item_name":""""
]
Fields = [
""""+created_at"+:"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d([\+\-]\d\d:\d\d)?)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""created_by":[^\}]+?"login":"(anonymous|Unknown User|({user}[^\s@"]+))"""
"""created_by":[^\}]+?"login":"({email_address}[^\s@"]+@[^\s@"]+)"""
"""\ssuser=(anonymous|({user}[^\s@"]+))\s+(\w+=|$)"""
"""\ssuser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
""""item_name":"({file_name}[^\.]+?)",""""
""""item_name":"([^\.]+?|(({file_name}[^"]+?\.(|({file_ext}[^\."]+?)))))",""""
""""item_type":"({file_type}[^"]+)"""
"""\sfname=({file_name}.+?)\s+(\w+=|$)"""
""""parent":\{[^\}]*?"name":"({file_dir}[^"]+)"""
""""event_type":"({access}[^"]+)"""
"""additional_details":\{[^\}]*?"size":({bytes}\d+)"""
"""(\||\s)requestClientApplication=({app}[^=]+?)(\s+\w+=|\s*$)"""
""""service_name":"({service_name}[^"]+)"""
""""shared_link_id":"({resource}[^,"\s]+?)""""
"""\smsg=({additional_info}.*?)\s\w+="""
"""owned_by"+:.+?"login"+:"+({dest_email_address}[^\s@"]+@[^\s@"]+)"""
"""[^\w]created_by"+\s*:\s*[^\}]+?[^\w]name"+\s*:\s*"+(Unknown User|({full_name}[^":,]+))[",\]\}]"""
"""[^\w]created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+.*?@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))"""
""""user":\{[^\}]+?"name":"({full_name}[^"]+)","email":"({email_address}[^@]+@({email_domain}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```