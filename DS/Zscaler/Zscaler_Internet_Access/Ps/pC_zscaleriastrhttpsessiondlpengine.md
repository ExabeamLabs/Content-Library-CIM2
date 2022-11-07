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
    """({time}\d\d\d\d-\d\d-\d\d\d\d:\d\d:\d\d)\s+reason="""
  ]

s-zscaler-web-activity = {
  Vendor = Zscaler
  Product = Zscaler Internet Access 
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d+:\d+:\d+)\s+(\w+=|$)""",
    """\sreason=(Allowed|({failure_reason}[^=]+?))\s*(\w+=|$)""",
    """\saction=({action}[^=]+?)\s*(\w+=|$)""",
    """\sprotocol=({protocol}[^=]+?)\s*(\w+=|$)""",
    """\srequestsize=({bytes_out}\d+)""",
    """\sresponsesize=({bytes_in}\d+)""",
    """\surlsupercategory=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+|$)""",
    """\surlcategory=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+|$)""",
    """\sserverip=(?:0.0.0.0|({dest_ip}[A-Fa-f\d:.]+))""",
    """\srequestmethod=(NA|({method}[^=]+?))\s*(\w+=|$)""",
    """\srefererURL=(?:None|({referrer}[^\s]+))\s*(\w+=|$)""",
    """\suseragent=(Unknown|({user_agent}[^=]+?))\s*(\w+=|$)""",
    """\sstatus=({http_response_code}\d+)""",
    """\sclientpublicIP=({src_ip}[A-Fa-f:\d.]+)""",
    """\sClientIP=({src_ip}[A-Fa-f\d:.]+)""",
    """\suser=({domain}[\w.\-]+)->({user}[^=]+?)(\s+\w+=|\s*$)""",
    """\suser=(?![^\s]+@[^\s]+)({user}[^\s]+)\s*(\w+=|$)""",
    """\suser=(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s@]+)\s*(\w+=|$)""",
    """\surl=(?:None|({url}[^\s]+))\s*(\w+=|$)""",
    """\surl=(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s]+)""",
    """\surl=(\w+:\/+)?[^|\/:]+(:\d+)?[^|?]+({uri_query}\?[^\s]+)""",
    """\shostname=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}\S+))""",
    """\spagerisk=({risk_level}\d+)""",
    """\sfileclass=(?:None|({mime}[^=]+?))\s*(\w+=|$)""",
    """\sappname=({app}[^=]+?)\s+(\w+|$)""",
    """\slocation=({location}[^=]+?)\s+\w+="""
  
}
```