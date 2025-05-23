#### Parser Content
```Java
{
Name = trendmicro-officescan-cef-alert-trigger-success-dlp
  ParserVersion = v1.0.0
  Product = OfficeScan
  Conditions = [ """|Trend Micro|""", """|Data Loss Prevention|""" ]

cef-trendmicro-dlp-alert = {
  Vendor = Trend Micro
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+[\+\-]\d+:\d+)""",
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\Wdvchost=({host}[^\s]+)""",
    """\Wcs4=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wshost=({src_host}.+?)\s+(\w+=|$)""",
    """\Wfname=({file_name}.+?)\s+(\w+=|$)""",
    """\WfilePath=({file_path}.+?)\s+(\w+=|$)""",
    """\Wcs5=({alert_name}.+?)\s+(\w+=|$)""",
    """CEF:([^\|]*\|){5}({alert_type}[^\|]+)""",
    """\WflexString2=({alert_type}.+?)\s+(\w+=|$)""",
    """\WflexString1=({result}.+?)\s+(\w+=|$)""",
    """\|Trend Micro\|Control Manager\|([^|]*\|){3}({alert_severity}[^|]+)\|""",
    """\Wcs1=({policy_guid}.+?)\s+(\w+=|$)""",
    """\WdeviceFacility=({additional_info}.+?)\s+(\w+=|$)""",
    """\Wduser=({target}.+?)\s+(\w+=|$)""",
    """\Wsuser=({last_name}[^,\(]+),\s*({first_name}[^,\)\=]+?)(\s*\([^\)]*\))?\s+(\w+=|$)""",
   ]
 }

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
    """\Wdst=(::|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wsrc=(::|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s""",
    """\Wspt=({src_port}\d+)""",
    """\Wact=(Unknown|({result}[^=]+?))(?:\s+\w+=|\s*$|\s*")""",
    """\Wcn3=({threat_type}[^=]+?)(\s+\w+=|\s*$|\s*")""",
    """\Wrequest="*(|({malware_url}[^"]+?))(\s+\w+=|\s*$|\s*"|”\]+\s+\w+=)""",
    """\WdeviceProcessName =({process_path}({process_dir}[^=]*?)({process_name}[^\/\\=]+?))(\s+\w+=|\s*$|\s*")""",
    """\sduser=((\d{1,3}\.){3}\d{1,3}|({email_address}[^@\s]+@[^\.\s]+\.[^\s]+?)|((({email_domain}[^\s\\\/=]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\s+\w+=|\s*$)""",
    """\sfilePath=({malware_url}[^=]+?)(\s+\w+=|\s*$)""",
    """\sfileHash=({hash_md5}\w+)(\s+\w+=|\s*$)"""
  
}
```