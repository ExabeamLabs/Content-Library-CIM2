#### Parser Content
```Java
{
Name = clearsense-cs-sk4-app-login-success-loginsuccessful
  Conditions = [ """SUCCESSFUL_LOGIN""", """Login Successful""", """requestClientApplication=ClearSense Audit""" ]
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
     """"+host"+:"+({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"+."+tenantUuid""",
     """"+host"+:"+({host}[^"]+)"+,"+user-agent"+:"+({user_agent}[^"]+)"+.+result"+:"+({result}[^"]+)""",
     """"+type"+:"+({operation}[^"]+)""",
     """"+resource"+:"+({resource}\{[^}]+\})"""
     """"+url"+:"+({additional_info}[^"]+?)""""

     ]
 
}
```