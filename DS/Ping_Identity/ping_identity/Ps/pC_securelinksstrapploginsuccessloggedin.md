#### Parser Content
```Java
{
Name = "securelink-s-str-app-login-success-loggedin"
  Conditions = [
    """ Logged in."""
    """SecureLink:"""
    """User:"""
  ]
  ParserVersion = "v1.0.0"

ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*(uid=({user}[^,]+)[^|]+?|AWSCentrifyAPI-Puppet|({=user}[^\s\|@]+))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*({email_address}[^\s\|@]+@({email_domain}[^\s\|@]+))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){1}\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({protocol}[^\s\|]+)"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){7}\s*({result}[^\s\|]+)"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){2}\s*(|({app}[^\|]*?))\s*\|"""
"""(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){5}\s*(|({host_ip}[A-Fa-f\d:.]*?)|({host}[\w\-.]+))\s*\|"""
]
DupFields = [
"protocol->auth_method"

}
```