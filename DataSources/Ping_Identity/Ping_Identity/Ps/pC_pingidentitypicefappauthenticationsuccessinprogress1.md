#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-authentication-success-inprogress-1
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions = [ """CEF""", """|Ping Identity|PingFederate|""", """|AUTHN_ATTEMPT|""", """msg=inprogress""" ]
  Fields = [
    """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)""",
    """\Wduid=({email_address}[^\s@]+@[^\s@]+)""",
    """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)""",
    """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)""",
    """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)""",
# tid is removed
    """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
  ]


}
```