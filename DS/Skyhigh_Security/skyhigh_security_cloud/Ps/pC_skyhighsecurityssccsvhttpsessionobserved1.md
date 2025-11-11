#### Parser Content
```Java
{
Name = skyhighsecurity-ssc-csv-http-session-observed-1
  Vendor = Skyhigh Security
  Product = Skyhigh Security Cloud
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """Logging-Client """, """http""", """OBSERVED""" ]
  Fields = [
    """({action}OBSERVED)""",
    """,({method}[^,]+),([^,]+,){4}OBSERVED"""
    """,({bytes_in}\d+),([^,]+,){3}OBSERVED"""
    """,({bytes_out}\d+),([^,]+,){2}OBSERVED"""
    """,({uri_path}[^,]+),OBSERVED"""
    """,OBSERVED,([^,]*,){2}({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """,OBSERVED,([^,]*,){3}({protocol}[^,]+)"""
    """,OBSERVED,([^,]*,){4}({category}[^,]+)"""
    """,OBSERVED,([^,]*,){5}({mime}[^,]+)"""
    """,OBSERVED,([^,]*,){9}({http_response_code}\d+)"""
    """,OBSERVED,([^,]*,){13}({browser}[^,]+)"""
    """,OBSERVED,([^,]*,){15}({user_agent}[^,]+)"""
    """,OBSERVED,([^,]*,){17}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """,OBSERVED,([^,]*,){18}({dest_port}\d+)"""

  ]


}
```