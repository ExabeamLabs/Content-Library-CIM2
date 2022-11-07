#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-login-success-sso
  Conditions = [ """CEF""", """|Ping Identity|PingFederate|""", """|SSO|""", """msg=success""" ]
  ParserVersion = "v1.0.0"

cef-ping-events-1 = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Fields = [
    """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wduid=({user}[^\s@\\\=]+?)[\\\=]*\s+(\w+=|$)""",
    """\Wduid=({email_address}[^\s@]+@[^\s@]+)""",
    """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)""",
    """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)""",
    """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)""",
    """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)""",
    """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)""",
  
}
```