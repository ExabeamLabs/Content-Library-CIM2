#### Parser Content
```Java
{
Name = pan-gp-cef-vpn-login-success-login
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd yyyy HH:mm:ss"]
  Conditions = [ """CEF:0|Palo Alto Networks|""", """|USERID|login|""" ]
  Fields = [
    """\sdvchost=({host}[\w.-]+?)\s+(\w+=|$)""",
    """\srt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2})\s""",
    """\sduser=(({domain}[^\\]+)\\+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """\sPanOSUserIdentifiedBySource=({email_address}[^@\s]+@[^\s=]+?)\s"""
    """\ssrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+(\w+=|$)""",
    """\sdst=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+(\w+=|$)""",
    """\scs1=({auth_method}[^=]+?)\scs1Label=MFAFactorType""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = v1.0.0


}
```