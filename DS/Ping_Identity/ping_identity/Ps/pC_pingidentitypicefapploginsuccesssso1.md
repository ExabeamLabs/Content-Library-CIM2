#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-login-success-sso-1
  Conditions = [ """CEF:""", """|Ping Identity|Ping Federate|""", """|SSO|""", """cs6=success""" ]
  ParserVersion = "v1.0.0"

cef-ping-events-1 = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = ["MMM dd yyyy HH:mm:ss.SSS","MMM. dd yyyy HH:mm:ss.SSS"]
  Fields = [
    """\Wrt=({time}\w+\.? \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wduid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\\\=]*\s+(\w+=|$)""",
    """\Wduid=({email_address}[^\s@]+@[^\s@]+)""",
    """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)""",
    """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)""",
    """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)""",
    """\|Ping Identity\|PingFederate\|([^\|]*){3}\|({event_name}[^\|]+)""",
    """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)""",
  
}
```