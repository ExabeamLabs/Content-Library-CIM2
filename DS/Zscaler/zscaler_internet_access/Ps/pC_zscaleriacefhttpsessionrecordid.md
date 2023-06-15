#### Parser Content
```Java
{
Name = zscaler-ia-cef-http-session-recordid
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""|LOGINNAME|""",
"""|CLIENTIP|""",
"""|URL|""",
"""|URLCAT|""",
"""|ACTION|""",
"""|ZSCALER|"""
  ]
  Fields = [
    """HOST\|({host}[^\|]+)""",
    """CONTENTTYPE\|([^\|]*\|){2}(NA|({user}[^\|]+?))\|(NA|({host}[\w\-.]+))""",
    """LOGINNAME\|(({email_address}[^\|]+@[^\|]+)|({user}[^\|\s]+))\|""",
    """REASON\|({proxy_action}[^\|]+)""",
    """ACTION\|({action}[^\|]+)""",
    """REQMETHOD\|(NA|({method}[^\|]+))""",
    """CLIENTIP\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """DESTINATIONIP\|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """PROTOCOL\|({protocol}[^|]+)""",
    """URL\|({url}[^|]+)""",
    """URL\|((\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({web_domain}[^\/:\|"]+))(:({dest_port}\d+))?(\/({uri_path}[^?\|\s]+))?(\?({uri_query}[^\|,]+))?\|""",
    """URLCAT\|({category}[^|]+)""",
    """USERAGENT\|(Unknown|({user_agent}[^|]+))""",
    """REQSIZE\|({bytes_out}\d+)""",
    """RESPCODE\|({http_response_code}\d+)""",
    """RESPSIZE\|({bytes_in}\d+)""",
    """APPNAME\|({app}[^|]+)""",
    """APPCLASS\|({app_group}[^|]+)""",
    """DLPDICT\|(None|({dlp_dict}[^|]+))""",
    """DLPENGINE\|(None|({dlp_eng}[^|]+))""",
    """LOCATION\|(None|({location}[^|]+))""",
    """DEPARTMENT\|(None|({department}[^|]+))""",
    """MALWARECAT\|(None|({malware_category}[^|]+))""",
    """CONTENTTYPE\|(None|({mime}[^\|]+))"""
    ]
  

}
```