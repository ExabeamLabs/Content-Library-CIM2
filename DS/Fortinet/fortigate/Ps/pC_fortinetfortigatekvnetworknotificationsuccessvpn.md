#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-network-notification-success-vpn
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """|vpn""" ]
 
fortinet-fortigate-cef-network-traffic-info {
 Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [ 
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\sCEF:""",
    """\Wstart=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """\Wtz="?({tz}[+-]\d+)"?"""
    """\Wdvchost=(|({host}.+?))(\s+[\w\.]+=|\s*$)""",
    """\Wproto=({protocol}\w+)""",
    """\Wsubtype=({sub_category}\w+)""",
    """\Wcat=({category}\w+)(\s+[\w\.]+=|\s*$)""",
    """\Wact=(|({action}.+?))(\s+[\w\.]+=|\s*$)""",
    """\Wshost=(|({src_host}[\w\-.]+?))(\s+[\w\.]+=|\s*$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wspt=({src_port}\d+)""",
    """\Wdhost=(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+?))(\s+[\w\.]+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdpt=({dest_port}\d+)""",
    """\WdeviceOutboundInterface=({dest_interface}.+?)(\s+[\w\.]+=|\s*$)""",
    """\WdeviceInboundInterface=({src_interface}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wout=({bytes_out}\d+)""",
    """\Win=({bytes_in}\d+)""",
    """xauthuser=(N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\Wsrccountry=((?i)reserved|({src_country}\w+))""",
    """\Wdstcountry=((?i)reserved|({dest_country}\w+))""",
    """CEF:([^\|]+\|){4}({event_code}[^\|]+)\|({event_name}[^\|]+)\|""",
    """\Wpolicyname=({policy_name}[^=]+)(\s+[\w\.]+=|\s*$)""",
    """\Wapp=({network_app}[^=]+)(\s+[\w\.]+=|\s*$)""",
    """\Wlogdesc=({additional_info}[^=]+)(\s+[\w\.]+=|\s*$)""",
    """\Wmsg=({status_msg}[^=]+)(\s+[\w\.]+=|\s*$)"""
  
}
```