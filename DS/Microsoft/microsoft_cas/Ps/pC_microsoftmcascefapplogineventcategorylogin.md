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
"""\ssuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
"""\srt=({time}\d{13})"""
"""destinationServiceName =({app}.+?)\s+\w+="""
"""\srequestClientApplication=(|({user_agent}.+?))\s+\w+="""
"""\sdvc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```