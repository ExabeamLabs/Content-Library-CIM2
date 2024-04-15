#### Parser Content
```Java
{
Name = "vms-openvms-kv-file-read-success-username"
Conditions = [
"""Auditable event:"""
"""Object access"""
"""Username:"""
]
ParserVersion = "v1.0.0"

sailpoint-iiq-events = {
  Vendor = Sailpoint
  Product = IdentityNow
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"ACCOUNT_NAME\\?":\\?"(({user_dn}(((CN|cn|uid)=[^"]+?),)?(({user_ou}(OU|ou)[^"]+?)?(DC|dc)=[\w-]+))|({account_id}[^"]+?)\\?")""",
    """"TARGET\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[^"\s]+?))\\?"""",
    """"SOURCE\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[^"\s]+?))\\?"""",
    """"APPLICATION\\?":\\?"({app}[^"]+?)\\?"""",
    """"ACTION\\?":\\?"({operation}[^"]+?)\\?""""
  
}
```