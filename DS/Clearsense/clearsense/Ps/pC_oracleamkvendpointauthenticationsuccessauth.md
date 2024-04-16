#### Parser Content
```Java
{
Name = "oracle-am-kv-endpoint-authentication-success-auth"
Conditions = [
""" IAU_RESOURCEHOST:"""
"""IAU_USERID:"""
""" IAU_EVENTTYPE:"""
""""Authentication""""
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
     """"+userName"+:"+({user}[\w\.\-]{1,40}\$?)""",
     """"+email"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
     """"+host"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+."+tenantUuid""",
     """"+host"+:"+({host}[^"]+)"+,"+user-agent"+:"+({user_agent}[^"]+)"+.+result"+:"+({result}[^"]+)""",
     """"+type"+:"+({operation}[^"]+)""",
     """"+resource"+:"+({resource}\{[^}]+\})"""
     """"+url"+:"+({additional_info}[^"]+?)""""

     ]
 
}
```