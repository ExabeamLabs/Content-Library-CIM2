#### Parser Content
```Java
{
Name = pan-gp-cef-endpoint-authentication-success-userauthentication
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  TimeFormat = "epoch"
  Conditions = [ """|Palo Alto Networks|""", """|globalprotect""", """user authentication succeeded""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """Login from:\s*({src_ip}[a-fA-F\d.:]+)""",
    """User name:\s+(({domain}[^\\]+)\\+)?({user}[\w.'\-\\$]+?)\.?(\s|,|"|$)""",
    """User name:\s+({email_address}[^@\s]+@[^\s,]+),""",
    """Client OS( version)?:\s+({os}[^":]+)(,|\.)"""
  ]
  ParserVersion = "v1.0.0"


}
```