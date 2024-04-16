#### Parser Content
```Java
{
Name = trendmicro-vone-cef-alert-trigger-success-visioone
  Vendor = Trend Micro
  Product = Vision One
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Trend Micro|Vision One|""", """900002|Vision One Observed Attack Technique|""" ]
  Fields = [
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^|]+)""",
    """CEF:([^\|]*\|){4}({event_code}[^|]+)""",
    """cat=((?i)Unknown|({alert_type}[^=,]+))(\s*,\S+)?\s+\w+=""",
    """dhost=({dest_host}[\w.-]+)\s""",
    """shost=({src_host}[\w.-]+)\s""",
    """flexString1=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? flexString1Label=Endpoint IPv4 Address""",
    """c6a1=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? c6a1Label=Endpoint IPv6 Address""",
    """act=(\[')?({action}[^=]+?)('\])?\s+\w+?=""",
    """filePath=({src_file_path}({file_dir}[^,]*?)[\\\/]*({src_file_name}[^\\]+?(\.({src_file_ext}[^\.\s]+))?))\s\w+=""",
    """dproc=\s*({process_command_line}[^=]+?)\s+\w+?=""",
    """reason=({additional_info}[^=]+)\s+\w+="""   
    """dvchost=({host}[\w.-]+)\s""",
    """dpt=({dest_port}\d+)"""
    """dst=\[?'*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """spt=({src_port}\d+)"""
    """src=\[?'*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
   ]


}
```