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
    """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wsrc="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdest="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wstatus="({http_response_code}\d+)""",
    """\Wrisk="({category}[^"]+)""",
    """\Whttp_protocol="({protocol}[^"]+)""",
    """\Whttp_method="({method}[^"]+)""",
    """\Wcategory="({category}[^"]+)""",
    """\Whttp_content_type="({mime}[^"]+)""",
    """\Whttp_user_agent="({user_agent}[^"]+)""",
    """\Wvirus_names="(|({malware_name}[^"]+))""",
    """\Waction="({action}[^"]+)""",
    """\Wblock_reason="({failure_reason}[^"]+)"""",
    """\Wreferrer="({referrer}[^"]+)""",
    """\Wurl="({url}[^"]+)""",
    """\Wurl="(\w+:\/+)?({web_domain}[^\/]+)({uri_path}[^"]+)""",
    """\Wurl="[^=|?]+({uri_query}\?[^\s"]+)"?\s""",
    """\Whttp_port="({dest_port}\d+)""",
    """\Wbytes_to_client="({bytes_in}\d+)""",
    """\Wbytes_from_client="({bytes_out}\d+)""",
  ]


}
```