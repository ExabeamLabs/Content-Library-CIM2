#### Parser Content
```Java
{
Name = "securelink-s-str-app-login-success-connected"
  Vendor = "SecureLink"
  Product = "SecureLink"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """SecureLink:"""
    """AUDIT:"""
    """connected to Application"""
  ]
  Fields = [
    """connected to Application ({app}[^\."]+)"""
    """AUDIT:.+?\(({email_address}[^@\)"]+@({email_domain}[^\)"]+))\)"""
  ]
  ParserVersion = "v1.0.0"


}
```