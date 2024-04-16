#### Parser Content
```Java
{
Name = zscaler-ia-cef-http-session-spriv
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [
"""|Zscaler|NSSWeblog|""",
"""requestClientApplication=""",
"""act="""
  ]
  Fields = [
    """({time}\d\d\d\d\s\w+\s\d{1,2}\s\d\d:\d\d:\d\d)\szscaler-nss""",
    """\srt=({time}\d+)""",
    """\srt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d ({host}\S+) CEF:""",
    """\sdvchost=(NA|({host}[\w\-.]+))\s*(\w+=|$|")""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(\w+=|$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(\w+=|$)""",
    """([^\|]*\|){5}({action}[^\|]+)""",
    """(\s|\|)act=({action}[^=]+?)\s*(\w+=|$)""",
    """\ssuser=(NA|None|\$NULL|(\w+[^=]+\->\w+[^=]+)\s|(?![^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?))\s*(\w+=|$)""",
    """\slogin=({email_address}[^@\s]+@[^@\s]+)\s\w+=""",
    """\ssuser=((noauth-protocol[^=]+)?(({email_address}[^@"]+@({email_domain}[^\."]+\.[^"\s]+))(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-]{1,40}\$?)))""",
    """\|({severity}\d+)\|act=""",
    """proto=({protocol}[^\s]+)""",
    """\seurl=({url}[^\s\/\?]+({uri_path}\/[^\?\s]+)?({uri_query}\?[^\s]+)?)""",
    """\sapp=({protocol}[^=]+?)\s*(\w+=|$)""",
    """\srequestProtocol=({protocol}[^=]+?)\s*(\w+=|$)""",
    """\scs4=(None|({ransomware_name}[^=]+?))\s*(\w+=|$)""",
    """\srequest=({url}[^\s]+?)\s+(\w+=|$)""",
    """\srequest=(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s]+)(\?\S+)?\s+(\w+=|$)""",
    """\srequest=[^=|?]+({uri_query}\?[^\s]+)\s""",
    """\srequest=(?:[^:?]+:\/+)?({web_domain}[^\/:\s]+)""",
    """\srequestMethod=(NA|({method}[^=]+?))\s*(\w+=|$)""",
    """\srequestClientApplication=([uU]nknown|({user_agent}[^=]+?))\s*(\w+=|$)""",
    """\scn1=({risk_level}\d+)""",
    """reqsize=({bytes_out}\d+)""",
    """respsize=({bytes_in}\d+)""",
    """\sout=({bytes_out}\d+)""",
    """\sin=({bytes_in}\d+)""",
    """\scat=({category}[^=]+?)\s+\w+=""",
    """\scontenttype=(None|Other|({mime}[^=]+?))\s*(\w+=|$)""",
    """\soutcome=({http_response_code}\d+)""",
    """\sreason=({proxy_action}[^=]+?)\s*(\w+=|$)""",
    """\scs1=({department}[^=]+?)\s*(\w+=|$)""",
    """\scs2=({categories}[^=]+?)\s*(\w+=|$)""",
    """\scs5=(None|({alert_name}[^=]+?))\s*(\w+=|$)""",
    """\scs6=(None|({dlp_engine}[^=]+?))\s*(\w+=|$)""",
    """sourcehost=(NA|None|\$NULL|({src_host}[^=]+?))\s+destinationhost=""",
    """devicehostname=(NA|({src_host}[^\s"]+?))\s*(\w+=|$)""",
    """ZscalerNSSWeblogDLPDictionaries=(None|({web_log_dict}[^=]+?))\s*([\w.]+=|$)""",
    """requestContext=(None|({referrer}[^\s]+?))(\|[\w-]+\||\s\w+=|\s*$)""",
    """\sdhost=[^=]*?({top_domain}[^\.]+\.\w+)\s+\w+=""",
    """\sspriv=({location}[^=]+?)\s\w+="""
    """DownloadFileName =(NA|None|({src_file_name}[^=\s]+))\s+"""
    """UploadFileName =(NA|None|({file_name}[^=\s]+))\s+"""
    """dlpdict=(NA|None|({dlp_dict}[^=\s]+))\s+"""
    """dlpengine=(NA|None|({dlp_engine}[^=\s]+))\s+"""
    """dlprulename=(NA|None|({rule}[^=\s]+))"""
  ]
  DupFields = ["ransomware_name->threat_category", "risk_level->suspicious_content"]


}
```