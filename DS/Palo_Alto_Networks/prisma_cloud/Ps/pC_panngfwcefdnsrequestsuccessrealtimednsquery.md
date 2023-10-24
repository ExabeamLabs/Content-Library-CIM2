#### Parser Content
```Java
{
Name = pan-ngfw-cef-dns-request-success-realtimednsquery
  Vendor = "Palo Alto Networks"
  Product = "Prisma Cloud"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """|palo alto networks|LF|""", """|DNS|realtime_dns_query|""" ]
  Fields = [
    """\srt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s""",
    """\sPanOSDNSResolverIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = v1.0.0


}
```