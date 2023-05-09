#### Parser Content
```Java
{
Name = trendmicro-ds-cef-alert-trigger-success-codeexecution
 ParserVersion = v1.0.0
 Product = Deep Security
 Vendor = Trend Micro
 TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
 Conditions = [ """CEF:""", """Drupal Core Remote Code Execution Vulnerability""" ]
  Fields = [
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|(Unknown|({alert_severity}[^\|]+))""",
    """\WeventId=({alert_id}\d+)""",
    """\Wdvc=({host}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """\Wdvchost=({host}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """rt=({time}\w+\s+\d\d \d\d\d\d \d\d:\d\d:\d\d \S+)""",
    """\sshost=(((\d{1,3}\.){3}\d{1,3}|({src_host}[\w\-.]+))|({additional_info}[^@]+@[^\s]+))\s+\w+=""",
    """\sdhost=((\d{1,3}\.){3}\d{1,3}|({dest_host}[\w\-.]+))\s+\w+=""",
    """\Wapp=({app}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """\Wdst=(::|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=(::|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s""",
    """\Wspt=({src_port}\d+)""",
    """\Wact=(Unknown|({result}[^=]+?))(?:\s+\w+=|\s*$|\s*")""",
    """\Wcn3=({threat_type}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """\Wrequest="*(|({malware_url}[^"]+?))(\s+\w+=|\s*$|\s*"|”\]+\s+\w+=)""",
    """\WdeviceProcessName =({process_path}({process_dir}[^=]*?)({process_name}[^\/\\=]+?))(\s+\w+=|\s*$|\s*")""",
    """\sduser=((\d{1,3}\.){3}\d{1,3}|({email_address}[^@\s]+@[^\.\s]+\.[^\s]+?)|((({domain}[^\s\\\/=]+)[\\\/]+)?({user}[^\s]+?)))(\s+\w+=|\s*$)""",
    """\sfilePath=({malware_url}[^=]+?)(\s+\w+=|\s*$)""",
    """\sfileHash=({hash_md5}\w+)(\s+\w+=|\s*$)"""
 ]
 

}
```