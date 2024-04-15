#### Parser Content
```Java
{
Name = "microsoft-o365-cef-file-read-success-fileaccessed-1"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""destinationServiceName =Office 365"""
"""flexString1=FileAccessed"""
"""sourceServiceName =OneDrive"""
]
Fields = [
""""CreationTime\\*"+:\\*\s*"+({time}[^\\"]+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\w) [\w\-.]+ """
"""\Wfname=\s*({file_name}.+?(\.({file_ext}[^\.\s]+))?)\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsuser=(({email_address}[^\s@]+@[^\s@]+)|({user}[^\s]+?))\s+(\w+=|$)"""
""""+UserId"+:"+({email_address}[^@\s"]+?@[^@\s"]+?)"+"""
"""\WfilePath=({file_path}.+?)\s+(\w+=|$)"""
"""\WfilePath=\{"ObjectUrl":"({file_path}[^"]+?)""""
"""\WrequestClientApplication=({process_name}.+?)\s+(\w+=|$)"""
"""\WfileType=({file_type}.+?)\s+(\w+=|$)"""
"""\WflexString1=({access}.+?)\s+(\w+=|$)"""
"""\Wmsg=[^=]*?\swas ({access}[^=]+?) by"""
]
ParserVersion = "v1.0.0"


}
```