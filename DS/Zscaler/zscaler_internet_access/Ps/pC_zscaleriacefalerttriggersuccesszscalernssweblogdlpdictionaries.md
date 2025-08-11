#### Parser Content
```Java
{
Name = zscaler-ia-cef-alert-trigger-success-zscalernssweblogdlpdictionaries
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Zscaler|NSSWeblog|""", """requestClientApplication=""", """act=""", """ZscalerNSSWeblogDLPDictionaries=""" ]
  Fields = [
    """\srt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d ({host}\S+) CEF:""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(\w+=|$)""",
    """([^\|]*\|){5}({action}[^\|]+)\|""",
    """(\s|\|)act=({action}[^=]+?)\s*(\w+=|$)""",
    """\ssuser=(NA|None|\$NULL|(\w+[^=]+\->\w+[^=]+)\s|(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)""",
    """\slogin=({email_address}[^@\s]+@[^@\s]+)\s\w+=""",
    """\ssuser=((noauth-protocol[^=]+)?(({email_address}[^@"]+@({email_domain}[^\."]+\.[^"\s]+))(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """\ssuser=((noauth-protocol[^=]+)?(({email_address}([A-Za-z0-9]+[!#$&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """\|({alert_severity}\d+)\|act=""",
    """\seurl=({url}[^\s\/\?]+({uri_path}\/[^\?\s]+)?({uri_query}\?[^\s]+)?)""",
    """\sapp=({protocol}[^=]+?)\s*(\w+=|$)""",
    """\srequest=({url}[^\s]+?)\s+(\w+=|$)""",
    """\srequest=(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s]+)(\?\S+)?\s+(\w+=|$)""",
    """\srequest=[^=|?]+({uri_query}\?[^\s]+)\s""",
    """\srequest=(?:[^:?]+:\/+)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^\/:\s]+))""",
    """\srequestMethod=(NA|({method}[^=]+?))\s*(\w+=|$)""",
    """\srequestClientApplication=([uU]nknown|({user_agent}[^=]+?))\s*(\w+=|$)""",
    """\scn1=({risk_level}\d+)""",
    """\sout=({bytes_out}\d+)""",
    """\sin=({bytes_in}\d+)""",
    """\scat=({category}[^=]+?)\s*(\w+=|$)""",
    """\scontenttype=(None|Other|({mime}[^=]+?))\s*(\w+=|$)""",
    """\soutcome=({http_response_code}\d+)""",
    """\sreason=({proxy_action}[^=]+?)\s*(\w+=|$)""",
    """\scs2=({categories}[^=]+?)\s*(\w+=|$)""",
    """\scs3=({category}[^=]+?)\s*(\w+=|$)""",
    """\scs6=({alert_type}[^=]+?)\s*(\w+=|$)""",
    """devicehostname=(NA|({src_host}[^\s"]+?))\s*(\w+=|$)""",
    """ZscalerNSSWeblogDLPDictionaries=({alert_name}[^=]+?)\s*([\w.]+=|$)""",
    """requestContext=(None|({referrer}[^\s]+?))(\|[\w-]+\||\s\w+=|\s*$)""",
    """\sdhost=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({web_domain}[^=\s]+\.\w+))\s+\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(\w+=|$)""",
    """\sspriv=({location}[^=]+?)\s*(\w+=|$)"""
    """DownloadFileName =(NA|None|({src_file_name}[^=\s]+))\s+"""
    """UploadFileName =(NA|None|({file_name}[^=\s]+))\s+"""
    """UploadFileName =(NA|None|({file_name}[^"]+?(\.({file_ext}[^"]+)))?) dlpdict"""
    """dlpdict=(NA|None|({alert_type}[^=]+?))\s*(\w+=|$)"""
    """dlprulename=(NA|None|({rule}[^=]+?))\s*(\w+=|$)"""
    """\sfileType=(None|({file_type}[^=]+?))\s*(\w+=|$)"""
    """\scn1=({risk_score}\d+)\scn1Label=riskscore"""
    """\sdeviceowner=(None|NA|({owner_id}[^=]+?))\s*(\w+=|$)"""
    """\sreason=({additional_info}[^=]+?)\s*(\w+=|$)"""
    """dlpengine=(NA|None|({additional_info}[^=\s]+?))\s*(\w+=|$)"""
  ]


}
```