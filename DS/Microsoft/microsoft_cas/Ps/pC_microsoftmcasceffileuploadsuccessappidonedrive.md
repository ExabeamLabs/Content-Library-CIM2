#### Parser Content
```Java
{
Name = "microsoft-mcas-cef-file-upload-success-appidonedrive"
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""cs2=APPID_ONEDRIVE"""
"""|MCAS|SIEM_Agent|"""
"""|EVENT_CATEGORY_UPLOAD_FILE|"""
]
Fields = [
"""SIEM_Agent\|[^|]+?\|({access}[^\|]+)\|"""
"""msg=(.+?):\s*({file_type}[^\s]+)\s*({file_dir}[^=]+)[\\\/]+({file_name}.*?\.({file_ext}[^\\:\s.]+)?)\s+(?:$|\w+=)"""
"""msg=(.+?):\s*({file_type}[^\s]+)\s*({file_path}.+?)\s+\w+="""
"""\ssuser=({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch)))\s+"""
"""\srt=({time}\d{13})"""
"""destinationServiceName =({app}.+?)\s+\w+="""
"""\srequestClientApplication=({user_agent}.+?)\s+\w+="""
"""\sdvc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wmsg=({additional_info}.*?)\s+(\w+=|$)""",
]
ParserVersion = "v1.0.0"


}
```