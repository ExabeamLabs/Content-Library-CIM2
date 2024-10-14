#### Parser Content
```Java
{
Name = microsoft-iis-cef-http-session-internetinformationserver
  Vendor = Microsoft
  Product = Microsoft IIS
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Microsoft|Internet Information Server|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdvc=({host}.+?)(\s+\w+=|\s*$)""",
    """\sdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """\sdeviceSeverity=({http_response_code}\d+)(\s+\w+=|\s*$)""",
    """\sshost=({src_host}.+?)(\s+\w+=|\s*$)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssuser=(({email_address}[^=@]+@[^=@]+?)|(({domain}[^=\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\sdpt=({dest_port}\d+)""",
    """\srequest=({uri_path}[^=\?]+?)({uri_query}\?.*?)?(\s+\w+=|\s*$)""",
    """\srequestMethod=({method}.+?)(\s+\w+=|\s*$)""",
    """\srequestClientApplication=({user_agent}.+?)(\s+\w+=|\s*$)""",
    """\scs1=({referrer}.+?)(\s+\w+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```