#### Parser Content
```Java
{
Name = onelogin-o-json-app-notification-lastslogin
  Product = OneLogin
  Vendor = OneLogin
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"distinguished_name":""", """"last_login":""", """"password_changed_at":""", """"invalid_login_attempts":""" ]
  Fields = [
    """"samaccountname":\s*"({user}[\w\.\-]{1,40}\$?)""",
    """"(userprincipalname|email|username)":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"company":\s*"({company}[^"]+?)\s*""",
    """"employeeID":\s*"({employee_id}[^"]+)""",
    """"lastname":\s*"({last_name}[^"]+?)\s*""",
    """"distinguished_name":\s*"({user_ou}[^"]+)""",
    """"created_at":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
# invalid_login_attempts is removed
# title is removed
    """"firstname":\s*"({first_name}[^"]+?)\s*""",
# password_changed_at is removed
# last_login is removed
    """"department":\s*"({department}[^"]+)""",
  ]


}
```