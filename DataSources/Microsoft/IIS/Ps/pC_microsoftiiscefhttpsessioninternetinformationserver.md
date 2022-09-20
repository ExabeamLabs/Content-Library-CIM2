#### Parser Content
```Java
{
Name = microsoft-iis-cef-http-session-internetinformationserver
  Vendor = Microsoft
  Product = IIS
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft|Internet Information Server|""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}.+?)(\s+\w+=|\s*$)""",
    """\sdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """\sdeviceSeverity=({http_response_code}\d+)(\s+\w+=|\s*$)""",
    """\sshost=({src_host}.+?)(\s+\w+=|\s*$)""",
    """\ssrc=({src_ip}[a-fA-F\d.:]+)""",
    """\ssuser=(({email_address}[^=@]+@[^=@]+?)|(({email_domain}[^=\\\/]+)[\\\/]+)?({user}[^=]+?))(\s+\w+=|\s*$)""",
    """\sdpt=({dest_port}\d+)""",
    """\srequest=({uri_path}[^=\?]+?)({uri_query}\?.*?)?(\s+\w+=|\s*$)""",
    """\srequestMethod=({method}.+?)(\s+\w+=|\s*$)""",
    """\srequestClientApplication=({user_agent}.+?)(\s+\w+=|\s*$)""",
    """\scs1=({referrer}.+?)(\s+\w+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```