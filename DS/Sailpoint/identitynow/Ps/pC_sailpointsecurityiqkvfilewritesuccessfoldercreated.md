#### Parser Content
```Java
{
Name = "sailpoint-securityiq-kv-file-write-success-foldercreated"
Conditions = [
"""| applicationtype : OneDrive """
"""actiontype : Folder Created"""
]
ParserVersion = "v1.0.0"

sailpoint-iiq-events = {
  Vendor = Sailpoint
  Product = IdentityNow
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """"ACCOUNT_NAME\\?":\\?"(({user_dn}(((CN|cn|uid)=[^"]+?),)?(({user_ou}(OU|ou)[^"]+?)?(DC|dc)=[\w-]+))|({account_id}[^"]+?)\\?")""",
    """"TARGET\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[\w\.\-]{1,40}\$?))\\?"""",
    """"SOURCE\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[\w\.\-]{1,40}\$?))\\?"""",
    """"APPLICATION\\?":\\?"({app}[^"]+?)\\?"""",
    """"ACTION\\?":\\?"({operation}[^"]+?)\\?""""
  
}
```