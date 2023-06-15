#### Parser Content
```Java
{
Name = pan-gp-cef-endpoint-authentication-success-userauthentication
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "epoch"
  Conditions = [ """|Palo Alto Networks|""", """|globalprotect""", """user authentication succeeded""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """Login from:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User name:\s+(({domain}[^\\]+)\\+)?({user}[\w.'\-\\$]+?)\.?(\s|,|"|$)""",
    """User name:\s+({email_address}[^@\s]+@[^\s,]+),""",
    """Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
  ]
  ParserVersion = "v1.0.0"


}
```