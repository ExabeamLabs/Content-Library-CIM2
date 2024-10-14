#### Parser Content
```Java
{
Name = "microsoft-o365-kv-user-password-modify-success-changeduserpassword"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""SESSID="""
"""RESULTCODE="""
"""WORKLOAD="""
"""COMMAND=Change user password."""
"""OBJECT="""
]
Fields = [
"""\sTS=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""USER=(Unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s]+))?)\s+\w+="""
"""DOMAIN=(|({domain}[^\s]+?))\s+\w+="""
"""WORKLOAD=({app}[^=]+?)\s+\w+="""
"""COMMAND=({event_name}[^=]+?)\s+\w+="""
"""OBJECT=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^=]+?))\s+\w+="""
"""SIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""RESULTCODE=({result}[^=]+?)\s+\w+="""
"""USERAGENT=\s*(|({user_agent}[^\n]+?))\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```