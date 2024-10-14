#### Parser Content
```Java
{
Name = "microsoft-o365-cef-file-success-fileoperation"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft|||"""
"""cat=SharePointFileOperation"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\scs5=({app}.+?)\s+\w+="""
"""\sact=({access}.+?)\s+\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s]+))?\s+\w+="""
"""\sfilePath=({src_file_path}.+?)\s+\w+="""
"""\sfilePath=(?: |({file_dir}[^=]+)[\\\/]+[^\\\/=]+)\s+\w+="""
"""\sfileType=({file_type}.+?)\s+\w+="""
"""\soldFileName =({src_file_name}.+?)\s+\w+="""
"""\soldFileType=({src_file_ext}.+?)\s+\w+="""
]
DupFields = [
"access->event_code"
]
ParserVersion = "v1.0.0"


}
```