#### Parser Content
```Java
{
Name = sailpoint-iiq-json-user-password-modify-success-target
  ParserVersion = "v1.0.0"
  Vendor = Sailpoint
  Product = SailPoint IIQ
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"ATTRIBUTE_NAME""", """"password""", """"ACCOUNT_NAME""", """"APPLICATION""", """"OWNER""", """"ACTION""", """"TARGET""", """"SOURCE""" ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
    """exabeam_host=([^=]+?@\s*)?({host}[\w.-]+)""",
    """"ACCOUNT_NAME\\?":\\?"(({user_dn}(((CN|cn|uid)=[^"]+?),)?(({user_ou}(OU|ou)[^"]+?)?(DC|dc)=[\w-]+))|({account_id}[^"]+?)\\?")""",
    """"TARGET\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[^"\s]+?))\\?"""",
    """"SOURCE\\?":\\?"(({email_address}[^@"]+@[^"]+?)|({user}[^"\s]+?))\\?"""",
    """"APPLICATION\\?":\\?"({app}[^"]+?)\\?"""",
    """"ACTION\\?":\\?"({operation}[^"]+?)\\?""""
  ]
  DupFields = [ "operation->event_name" ]


}
```