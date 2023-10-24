#### Parser Content
```Java
{
Name = sailpoint-identitynow-json-endpoint-authentication-auth
Conditions = [
  """type": "AUTH"""
  """stack": """
  """attributes":"""
]
ParserVersion = "v1.0.0"

auth0-authentication-template = {
    Vendor = Auth0
    Product = Auth0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)""",
      """hostname"+:"+({host}[^"]+)""",
      """description"+:"+({additional_info}[^"]+)\s*"+""",
      """"+ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """user_name"+:"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"""",     
      """user_id"+:"+((({auth_type}[^|"]+)\|({domain}[^|"]+)\|({user}[\w\.\-]{1,40}\$?))|(({=auth_type}[^|"]+)\|))"""
      """client_name"+:"+({app}[^"]+)""",
      """user_agent"+:"+({user_agent}[^"]+)""",         
      """severity"+:"+({alert_severity}[^"]+)""", 
      """"type":"({operation_type}[^",]+)""""
    
}
```