#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-logout-success-pingfederate
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions = [ """CEF:""", """|Ping Identity|PingFederate|""", """|SRI_REVOKED|""", """ msg=success """ ]
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """({event_name}SRI_REVOKED)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wduid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\\\=]*\s+(\w+=|$)""",
    """\Wduid=({email_address}[^\s@]+@[^\s@]+)""",
    """\Wcs2=(|({connection_id}[^=]+?))\s+(\w+=|$)""",
    """\Wcs3=(|({protocol}[^=]+?))\s+(\w+=|$)""",
    """\Wmsg=(|({result}[^=]+?))\s+(\w+=|$)""",
    """externalId=({tid}[^=]+)\s+\w+=""",
    """cs6=(|({additional_info}[^"]+?))\s+(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```