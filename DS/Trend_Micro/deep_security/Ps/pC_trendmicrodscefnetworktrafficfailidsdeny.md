#### Parser Content
```Java
{
Name = trendmicro-ds-cef-network-traffic-fail-idsdeny
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = Deep Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """|Trend Micro|Deep Security Agent|""", """act=IDS:Deny""", """CEF:""" ]
  Fields = [
    """\d\d:\d\d\s({host}.+?)\sCEF:""",
    """proto=({protocol}.+?)(\s+\w+=|\s*$)""",
    """in=({bytes_in}\d+)""",
    """out=({bytes_out}\d+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dmac=({dest_mac}[^\s]+)""",
    """smac=({src_mac}[^\s]+)""",
    """dvchost=({dest_host}[^\s]+)""",
    """act=IDS:({operation}[^\s]+)""",
    """cs2=({method}[^\s]+)""",
    """CEF.*?\|(.*?\|){4}({rule}.+?)\|"""
    """dpt=({dest_port}\d+)"""
    """spt=({src_port}\d+)"""
    """cs1=({additional_info}.+?)\s\w+=""",
    """suser=(NT AUTHORITY\\+SYSTEM|({user}[\w\.\-]{1,40}\$?))""",
    """fileHash=({file_hash}[^\s]+)""",
    """cs3=({hash_md5}[^\s]+)""",
    """cs2=({hash_sha1}[^\s]+)""",
    """suid=({suid}.+?)\s\w+=""",
    """filePath=({file_path}({file_dir}[^,]*?)[\\\/]*({file_name}[^\\]+?(\.({file_ext}[^\.\s]+))?))\s\w+="""
  ]
  DupFields = ["rule->failure_reason"]


}
```