#### Parser Content
```Java
{
Name = microsoft-iis-str-http-session-webactivity
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft IIS
  TimeFormat = "yyyy-MM-dd 'time' HH:mm:ss"
  Conditions = [ """ s-sitename """, """ s-computername """,""" cs-bytes """,""" cs(Referer) """,""" cs(User-Agent) """ ]
  Fields = [
    """date\s({time}\d\d\d\d-\d\d-\d\d\stime\s\d\d:\d\d:\d\d)""",
    """\scs-host\s(-|({web_domain}[^\s]+))\s""",
	"""\sc-ip\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """\ss-ip\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """\scs-username\s(-|(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """\ss-port\s(-|({dest_port}\d{1,5}))\s""",
    """\scs-method\s({method}[^\s]+)\s""",
    """\ssc-status\s(-|({result_code}\d{1,5}))\s""",
    """\ssc-bytes\s({bytes_out}\d+)\s""",
    """\scs-bytes\s({bytes_in}\d+)\s""",
    """\scs\(User-Agent\)\s({user_agent}[^\s]+)\s"""
    """\scs\(Referer\)\s(-|({referrer}[^\s]+))\s""",
    """\scs-uri-query\s(-|({uri_query}[^\s]+?))\s""",
    """\scs-uri-stem\s(-|\/|({uri_path}[^\s]+?))\s""",
    """\ss-computername\s({dest_host}[^\s]+)\s""",
  ]


}
```