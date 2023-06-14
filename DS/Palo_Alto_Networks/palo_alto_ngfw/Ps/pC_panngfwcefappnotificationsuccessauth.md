#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-notification-success-auth
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:0|Palo Alto Networks|""", """|SYSTEM|auth|""", """saml-client-redirect"""]
  Fields = [
    """\sdvchost=({host}[\w.-]+?)\s+(\w+=|$)""",
    """rt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2})\s""",
    """Client '({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))' redirected to""",
    """act=({operation}saml-client-redirect)""",
    """msg=({additional_info}[^=]+)\s+(\w+=|$)""",
    """fname=({authentication_profile}[^=]+)\s+(\w+=|$)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```