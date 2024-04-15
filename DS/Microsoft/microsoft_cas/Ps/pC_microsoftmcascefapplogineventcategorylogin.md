#### Parser Content
```Java
{
Name = "microsoft-mcas-cef-app-login-eventcategorylogin"
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|MCAS|SIEM_Agent|"""
"""|EVENT_CATEGORY_"""
"""_LOGIN|"""
]
Fields = [
"""EVENT_CATEGORY_({result}.+?)_LOGIN"""
"""Failure message:\s*({failure_reason}.+?)\)\s+\w+="""
"""\ssuser=({user}[^@]+)@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))\s+"""
"""\srt=({time}\d{13})"""
"""\sdestinationServiceName =({app}.+?)\s+\w+="""
"""\srequestClientApplication=(|({user_agent}.+?))\s+\w+="""
"""\sdvc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```