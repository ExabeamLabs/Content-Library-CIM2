#### Parser Content
```Java
{
Name = "box-ccm-kv-file-operation"
Vendor = "Box"
Product = "Box Cloud Content Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""created_by_login="""
"""created_by_name="""
"""source_item_name="""
"""event_type="""
]
Fields = [
"""created_at=\"+({time}[^\"]+)\""""
"""created_by_login=\"+({user}[\w\.\-]{1,40}\$?)"""
"""accessible_by_login=\"+({object}[^\"@]+)"""
"""source_user_email=\"+({object}[^@]+)"""
"""({file_type}folder)"""
"""source_item_name=\"+({file_name}[^".]+\.?({file_ext}[^"]+|))"""
"""source_item_type=\"+({file_type}[^\"]+)"""
"""source_folder_name=\"+({file_name}[^\"]+)"""
"""source_parent_name=\"+({file_dir}[^\"]+)"""
"""additional_details_size=\"({bytes}\d+)"""
"""ip_address=\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""event_type=\"+({access}[^\"]+)"""
"""created_by_login=\"({email_address}.*?@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch)))"""
]
DupFields = [
"access->event_code"
"file_name->src_file_name"
"file_ext->src_file_ext"
]
ParserVersion = "v1.0.0"


}
```