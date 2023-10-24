#### Parser Content
```Java
{
Name = "dropbox-d-json-app-file-success-tag"
Vendor = "Dropbox"
Product = "Dropbox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""".tag":"""
""""file_operations"}"""
""""event_category":"""
""""event_type":"""
]
Fields = [
""""timestamp":\s*\"({time}[^\"]+)"""
""""actor":[^\}]*?\"display_name\":\s*\"(?:N\/A|({full_name}[^\"@]+))""""
""""actor":[^\}]*?\"email\":\s*\"(?:N\/A|({email_address}[^@\"\s]+@[^@\"\s]+))""""
""""event_type":\s*\{[^\\]*?\"\.tag\":\s\"({operation}[^\"]+)""""
""""description":\s*\"({additional_info}[^\"]+)\""""
""""ip_address":\s*\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""({app}Dropbox)"""
""""assets":\s*\[[^\]]*?\"display_name\":\s*\"({object}[^\"]+)""""
""""assets":\s*\[[^\]]*?\"contextual\":\s*\"({resource}[^\"]+)""""
]
ParserVersion = "v1.0.0"


}
```