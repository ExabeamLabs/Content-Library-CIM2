#### Parser Content
```Java
{
Name = "sap-s-cef-endpoint-authentication-logon"
Product = "SAP"
Conditions = [
"""CEF:"""
"""|SAP|Security Audit Log|"""
"""Logon"""
]
ParserVersion = "v1.0.0"

clesarsense-app-activity = {
   Vendor = Clearsense
   Product = Clearsense
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Fields = [
     """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
     """requestClientApplication=({app}.*?)\s*\w+=""",
     """"path":"({object}[^"]+?)""""
     """"+method"+:"+({method}[^"]+)""",
     """"+statusCode"+:({result}\d+)""",
     """"+userName"+:"+({user}[^@"]+)""",
     """"+email"+:"+({email_address}[^@]+@({email_domain}[^"]+))""",
     """"+host"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+."+tenantUuid""",
     """"+host"+:"+({host}[^"]+)"+,"+user-agent"+:"+({user_agent}[^"]+)"+.+result"+:"+({result}[^"]+)""",
     """"+type"+:"+({operation}[^"]+)""",
     """"+resource"+:"+({resource}\{[^}]+\})"""
     """"+url"+:"+({additional_info}[^"]+?)""""

     ]
 
}
```