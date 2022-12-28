#### Parser Content
```Java
{
Name = microsoft-azuread-cef-user-password-modify-success-changeuserpassword
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "epoch"
  Conditions = [ """|Microsoft|Azure Active Directory|""", """|Change user password|""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wact=({event_code}.+?)\s*(\w+=|$)""",
    """\Woutcome=({result}.+?)\s*(\w+=|$)""",
    """\Wsuid=(?!\S+@\S+)({user}[^\s]+)\s*(\w+=|$)""",
    """\Wsuid=({email_address}({user}[^\s@]+)@[^\s]+)\s*(\w+=|$)""",
    """\Wcs5=.+?\|/Target/ID:"({dest_user}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```