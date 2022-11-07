#### Parser Content
```Java
{
Name = trendmicro-dsa-cef-alert-trigger-success-moduleformatstring
  ParserVersion = v1.0.0
  Product = Deep Security Agent
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSZ"
  Conditions = [ """CEF:""", """Module Format String Vulnerability""" ]

cef-trendmicro-security-alert = {
  Vendor = Trend Micro
  TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
  Fields = [
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|(Unknown|({alert_severity}[^\|]+))""",
    """\WeventId=({alert_id}\d+)""",
    """\Wdvc=({host}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """\Wdvchost=({host}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """rt=({time}\w+\s+\d\d \d\d\d\d \d\d:\d\d:\d\d \S+)""",
    """\sshost=(((\d{1,3}\.){3}\d{1,3}|({src_host}[\w\-.]+))|({additional_info}[^@]+@[^\s]+))\s+\w+=""",
    """\sdhost=((\d{1,3}\.){3}\d{1,3}|({dest_host}[\w\-.]+))\s+\w+=""",
    """\Wapp=({app}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """\Wdst=(::|({dest_ip}[a-fA-F\d.:]+))\s""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=(::|({src_ip}[a-fA-F\d.:]+))\s""",
    """\Wspt=({src_port}\d+)""",
    """\Wact=(Unknown|({action}[^=]+?))(?:\s+\w+=|\s*$|\s*")""",
    """\Wcn3=({threat_type}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """\Wrequest="*(|({malware_url}[^"]+?))(\s+\w+=|\s*$|\s*"|”\]+\s+\w+=)""",
    """\WdeviceProcessName =({process_path}({process_dir}[^=]*?)({process_name}[^\/\\=]+?))(\s+\w+=|\s*$|\s*")""",
    """\sduser=((\d{1,3}\.){3}\d{1,3}|({email_address}[^@\s]+@[^\.\s]+\.[^\s]+?)|((({email_domain}[^\s\\\/=]+)[\\\/]+)?({user}[^\s]+?)))(\s+\w+=|\s*$)""",
    """\sfilePath=({malware_url}[^=]+?)(\s+\w+=|\s*$)""",
    """\sfileHash=({hash_md5}\w+)(\s+\w+=|\s*$)"""
  
}
```