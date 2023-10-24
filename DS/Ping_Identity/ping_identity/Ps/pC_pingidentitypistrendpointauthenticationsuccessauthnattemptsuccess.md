#### Parser Content
```Java
{
Name = pingidentity-pi-str-endpoint-authentication-success-authnattemptsuccess
Conditions = [
  """|AUTHN_ATTEMPT|"""
  """success|"""
]
ParserVersion = "v1.0.0"

ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d),"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[\w\.\-]{1,40}\$?)[^|]+?|AWSCentrifyAPI-Puppet|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({=user}[^\s\|@]+?))([@＠]({domain}[^\s\|]+))?\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}[A-Fa-f\d:.]*?)|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
"protocol->auth_method"

}
```