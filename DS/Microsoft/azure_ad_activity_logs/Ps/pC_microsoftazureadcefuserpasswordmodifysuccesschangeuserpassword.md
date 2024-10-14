#### Parser Content
```Java
{
Name = microsoft-azuread-cef-user-password-modify-success-changeuserpassword
  Vendor = Microsoft
  Product = Azure AD Activity Logs
  TimeFormat = "epoch"
  Conditions = [ """|Microsoft|Azure Active Directory|""", """|Change user password|""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wact=({event_code}.+?)\s*(\w+=|$)""",
    """\Woutcome=({result}.+?)\s*(\w+=|$)""",
    """\Wsuid=(?!\S+@\S+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\w+=|$)""",
    """\Wsuid=({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@[^\s]+)\s*(\w+=|$)""",
    """\Wcs5=.+?\|/Target/ID:"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"


}
```