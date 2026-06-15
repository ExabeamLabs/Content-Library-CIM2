#### Parser Content
```Java
{
Name = zscaler-ia-str-http-session-dlp-ai-apps
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = v1.0.0
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """module=AI & ML Apps""", """action=""", """DLPEng=""", """url=""", """login=""" ]
  Fields = [
    """({time}\w+\s+\w+\s+\d+\s+\d+:\d+:\d+\s+\d\d\d\d)""",
    """login=({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s""",
    """dname=({web_domain}[^=]+?)\s+(\w+=|$)""",
    """dip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """sip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """natPublicIp=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """ua=({user_agent}[^=]+?)(\s+\w+=|\s*$)""",
    """url=({url}(\w+:\/\/)?({web_domain}[^\/]+?)({uri_path}\/[^\?]*?)?({uri_query}\?[^,]+)?)(\s\w+=|\s*$)""",
    """module=({app_group}[^=]+?)(\s+\w+=|\s*$)""",
    """proto=({protocol}[^=]+?)(\s+\w+=|\s*$)""",
    """action=({action}[^=]+?)(\s+\w+=|\s*$)""",
    """action=({result}[^=]+?)(\s+\w+=|\s*$)""",
    """reason=({result_reason}[^=]+?)(\s+\w+=|\s*$)""",
    """appName =({app}[^=]+?)(\s+\w+=|\s*$)""",
    """appClass=({app_type}[^=]+?)(\s+\w+=|\s*$)""",
    """fileType=({file_type}[^=]+?)(\s+\w+=|\s*$)""",
    """reqSize=({bytes_out}\d+)(\s+\w+=|\s*$)""",
    """responseSize=({bytes_in}\d+)(\s+\w+=|\s*$)""",
    """totalSize=({bytes}\d+)(\s+\w+=|\s*$)""",
    """malwareCat=({malware_family}[^=]+?)(\s+\w+=|\s*$)""",
    """malwareClass=({malware_family}[^=]+?)(\s+\w+=|\s*$)""",
    """threatName =({alert_name}[^=]+?)(\s+\w+=|\s*$)""",
    """riskScore=({risk_score}\d+)(\s+\w+=|\s*$)""",
    """DLPEng=(None|({alert_name}[^=]+?))(\s+\w+=|\s*$)""",
    """DLPEng=(None|({policy_name}[^=]+?))(\s+\w+=|\s*$)""",
    """DLPDict=({dlp_dict}[^=]+?)(\s+\w+=|\s*$)""",
    """location=({location}[^=]+?)(\s+\w+=|\s*$)""",
    """dept=({department}[^=]+?)(\s+\w+=|\s*$)""",
    """reqMethod=({method}[^=]+?)(\s+\w+=|\s*$)""",
    """respCode=({http_response_code}\d+)(\s+\w+=|\s*$)""",
    """urlClass=({event_category}[^=]+?)(\s+\w+=|\s*$)""",
    """urlSuperCat=({categories}({category}[^=]+?)[^=]*?)(\s+\w+=|\s*$)""",
    """urlCat=({categories}({category}[^=]+?)[^=]*?)(\s+\w+=|\s*$)""",
    """referer=({referrer}[^\s]+)"""
  ]


}
```