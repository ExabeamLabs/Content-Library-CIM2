#### Parser Content
```Java
{
Name = zscaler-ia-kv-http-session-url
  ParserVersion = "v1.0.0"
  Conditions = [ """dlpengine=None""", """threatcategory=None""", """threatname=None""", """url=""" ]
  Fields = ${ZscalerParsersTemplates.s-zscaler-web-activity.Fields}[
    """\sodevicehostname=({src_host}[^\s]+)"""
    """\surl="*(?:None|({url}[^\s"]+))"*\s*(\w+=|$)""",
    """urlcategory=(Miscellaneous or Unknown|({category}[^=]+?))\s+(\w+=|$)""",
    """\surlcategory=({category}[^;,=]+?)\s*\w+=""",
    """\surl="*(\w+:\/+)?[^|\/:]+(:\d+)?[^|?]+({uri_query}\?[^\s"]+)""",
    """\sappname=({app}[^=]+?)\s+(\w+=|$)""",
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
    """\sprotocol=({protocol}[^=]+?)\s*(\w+=|$)""",
    """\srequestsize=({bytes_out}\d+)""",
    """\sresponsesize=({bytes_in}\d+)""",
    """\surlsupercategory=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+|$)""",
    """\surlcategory=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+|$)""",
    """\sserverip=(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\srequestmethod=(NA|({method}[^=]+?))\s*(\w+=|$)""",
    """\srefererURL=(?:None|({referrer}[^\s]+))\s*(\w+=|$)""",
    """\suseragent=(Unknown|({user_agent}[^=]+?))\s*(\w+=|$)""",
    """\sstatus=({http_response_code}\d+)""",
    """\sclientpublicIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sClientIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\suser=({domain}[\w.\-]+)->({user}[^=]+?)(\s+\w+=|\s*$)""",
    """\suser=(?![^\s]+@[^\s]+)({user}[^\s]+)\s*(\w+=|$)""",
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