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
  TimeFormat = ["MMM dd yyyy HH:mm:ss.SSS","MMM. dd yyyy HH:mm:ss.SSS"]
  Fields = [
    """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wduid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\\\=]*\s+(\w+=|$)""",
    """\Wduid=({email_address}[^\s@]+@[^\s@]+)""",
    """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)""",
    """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)""",
    """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)""",
    """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)""",
    """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)""",
  
}
```