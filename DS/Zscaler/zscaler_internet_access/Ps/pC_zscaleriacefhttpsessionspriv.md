#### Parser Content
```Java
{
Name = zscaler-ia-cef-http-session-spriv
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Zscaler|NSSWeblog|""", """requestClientApplication=""", """act=""", """cs6=None""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\srt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """(devicehostname|dvchost)=(NA|({host}[\w\-.]+))\s*(\w+=|$|")""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(\w+=|$)""",
    """act=({action}[^=\s]+)""",
    """suser=(NA|None|\$NULL|(\w+[^=]+\->\w+[^=]+)\s|(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)""",
    """login=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s\w+=""",
    """suser=((noauth-protocol[^=]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """\|({severity}\d+)\|act=""",
    """request=({url}[^\s\/\?]+({uri_path}\/[^\?\s]+)?({uri_query}\?[^\s]+)?)""",
    """app=({protocol}[^=\s]+)""",
    """requestProtocol=({protocol}[^=\s]+)""",
    """cs4=(None|({malware_name}[^=]+?))\s*(\w+=|$)""",
    """requestMethod=(NA|({method}[^\s=]+))""",
    """requestClientApplication=((?i)unknown|({user_agent}[^=]+?))\s+(\w+=|$)""",
    """cn1=({risk_level}\d+)""",
    """out=({bytes_out}\d+)""",
    """in=({bytes_in}\d+)""",
    """cat=({category}[^=]+?)\s+\w+=""",
    """contenttype=(None|Other|({mime}[^=]+?))\s+(\w+=|$)""",
    """outcome=({http_response_code}\d+)""",
    """reason=({proxy_action}[^=]+?)\s+(\w+=|$)""",
    """cs1=({department}[^=]+?)\s+(\w+=|$)""",
    """cs2=({categories}[^=]+?)\s+(\w+=|$)""",
    """cs5=(None|({alert_name}[^=]+?))\s+(\w+=|$)""",
    """cs6=(None|({dlp_engine}[^=]+?))\s+(\w+=|$)""",
    """sourcehost=(NA|None|\$NULL|({src_host}[^=]+?))\s+destinationhost=""",
    """ZscalerNSSWeblogDLPDictionaries=(None|({web_log_dict}[^=]+?))\s*([\w.]+=|$)""",
    """requestContext=(None|({referrer}[^\s]+?))(\|[\w-]+\||\s\w+=|\s*$)""",
    """dhost=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^=\s]+\.\w+))\s+\w+=""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(\w+=|$)""",
    """spriv=({location_area}({location}[^=]+?))\s\w+="""
    """DownloadFileName =(NA|None|({src_file_name}[^=\s]+))\s+"""
    """UploadFileName =(NA|None|({file_name}[^=\s"]+))\s+"""
    """UploadFileName =(NA|None|({file_name}[^"]+?(\.({file_ext}[^"]+)))?) dlpdict"""
    """dlpdict=(NA|None|({dlp_dict}[^=\s]+))\s+"""
    """dlpengine=(NA|None|({dlp_engine}[^=\s]+))\s+"""
    """dlprulename=(NA|None|({rule}[^=\s]+))"""
    """destinationServiceName =({network_app}[^=]+?)\s+\w+="""
    """fileType=(None|({file_type}[^=]+?))\s+\w+="""
    """cn1=({risk_score}\d+)\scn1Label=riskscore"""
    """deviceowner=(None|NA|({owner_id}[^=]+?))\s+\w+="""
    """cs4=(None|({malware_family}[^=]+?))\scs4Label=malwarecat"""
  ]


}
```