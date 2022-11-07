#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-authenticationmethod
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Web Gateway
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  Conditions = [ """mwg:""", """datetime="""", """authentication_method="""" ]
  Fields = [
    """\Wdatetime="\[({time}[^\[\]]+)""",
    """({host}[\w\-\.]+)\s*mwg:""",
    """\Wuser="({user}[^"]+)""",
    """\Wsrc="({src_ip}[a-fA-F:\d\.]+)""",
    """\Wdest="({dest_ip}[a-fA-F:\d\.]+)""",
    """\Wstatus="({http_response_code}\d+)""",
    """\Wrisk="({category}[^"]+)""",
    """\Whttp_protocol="({protocol}[^"]+)""",
    """\Whttp_method="({method}[^"]+)""",
    """\Wcategory="({category}[^"]+)""",
    """\Whttp_content_type="({mime}[^"]+)""",
    """\Whttp_user_agent="({user_agent}[^"]+)""",
    """\Wvirus_names="(|({ransomware_name}[^"]+))""",
    """\Waction="({action}[^"]+)""",
    """\Wblock_reason="({failure_reason}[^"]+)"""",
    """\Wreferrer="({referrer}[^"]+)""",
    """\Wurl="({url}[^"]+)""",
    """\Wurl="(\w+:\/+)?({web_domain}[^\/]+)({uri_path}[^"]+)""",
    """\Wurl="(\w+:\/+)?[^\|\/:]+(:\d+)?[^|?]+({uri_query}\?[^\s"]+)""",
    """\Whttp_port="({dest_port}\d+)""",
    """\Wbytes_to_client="({bytes_in}\d+)""",
    """\Wbytes_from_client="({bytes_out}\d+)""",
  ]


}
```