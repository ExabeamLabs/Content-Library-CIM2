#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-authentication-success-inprogress
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|Ping Identity|Ping Federate|""", """|AUTHN_ATTEMPT|""", """cs6=inprogress""" ]

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