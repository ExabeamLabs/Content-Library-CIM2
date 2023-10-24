#### Parser Content
```Java
{
Name = zscaler-ia-str-http-session-dlpengine
  ParserVersion = v1.0.0
  Conditions = [
"""dlpengine=None""",
"""vendor=Zscaler""",
"""event_id=""",
"""url=""" ]
  Fields = ${ZscalerParsersTemplates.s-zscaler-web-activity.Fields}[
    """({time}\d\d\d\d-\d\d-\d\d\d\d:\d\d:\d\d)\s+reason=""",
  ]

s-zscaler-web-activity = {
  Vendor = Zscaler
  Product = Zscaler Internet Access 
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """datetime=({time}\w{1,3}\s\w{1,3}\s{1,5}\d{1,2}\s\d\d:\d\d:\d\d\s\d{4})"""
    """devicehostname=(NA|({host}[\w\.\-]+))\s\w+=""",
    """({time}\d\d\d\d-\d\d-\d\d \d+:\d+:\d+)\s+(\w+=|$)""",
    """\sreason=(Allowed|({failure_reason}[^=]+?))\s*(\w+=|$)""",
    """\saction=({action}[^=]+?)\s*(\w+=|$)""",
    """\s(protocol|proto)=({protocol}[^=]+?)\s*(\w+=|$)""",
    """\s(requestsize|reqSize)=({bytes_out}\d+)""",
    """\s((?i)responsesize)=({bytes_in}\d+)""",
    """\s(urlsupercategory|urlSuperCat)=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+|$)""",
    """\s(urlcategory|urlCat)=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+|$)""",
    """\sserverip=(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\s(reqMethod|requestmethod)=(NA|({method}[^=]+?))\s*(\w+=|$)""",
    """\s(referer|refererURL)=(?:None|({referrer}[^\s]+))\s*(\w+=|$)""",
    """\s(ua|useragent)=(Unknown|({user_agent}[^=]+?))\s*(\w+=|$)""",
    """\s(respCode|status)=({http_response_code}\d+)""",
    """\sclientpublicIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sClientIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\suser=({domain}[\w.\-]+)->({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)""",
    """\suser=(?![^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)""",
    """\suser=(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s@]+)\s*(\w+=|$)""",
    """\surl=(?:None|({url}[^\s]+))\s*(\w+=|$)""",
    """\surl=(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s]+)""",
    """\surl=(\w+:\/+)?[^|\/:]+(:\d+)?[^|?]+({uri_query}\?[^\s]+)""",
    """\shostname=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}\S+))""",
    """\spagerisk=({risk_level}\d+)""",
    """\scontenttype=(?:None|({mime}[^=]+?))\s*(\w+=|$)""",
    """\sappname=({app}[^=]+?)\s+(\w+|$)""",
    """\slocation=({location}[^=]+?)\s+\w+="""
  
}
```