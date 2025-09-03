#### Parser Content
```Java
{
Name = "checkpoint-es-kv-alert-trigger-success-threatemulation-1"
  Vendor = "Check Point"
  Product = "Check Point Endpoint Security"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  ParserVersion = "v1.0.0"
  Conditions = [
    """|Check Point|Threat Emulation|"""
  ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+)"""
    """origin=({origin_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """Protection Name =({alert_name}[^\|]+)\|"""
    """(Protection Type|protection_type)=({alert_type}[^=]+?)\s*\w+="""
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """(s_port|srcPort)=({src_port}\d+)"""
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """service=({dest_port}\d+)"""
    """proto=({protocol}[^=]+?)\s*\w+="""
    """action=({action}[^=]+?)\s*\w+="""
    """method=({method}\w+)"""
    """http_host=({host}[^=]+?)\s*\w+="""
    """\Wsrc_user_name:"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[^"@\(\)]+@[\(\)^"@]+))\s*""""
    """user_agent=({user_agent}[^=]+?)\s*\w+="""
    """verdict=({result}\w+)"""
    """web_client_type=({client_type}[^=]+?)$"""
    """usrName =({full_name}.+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """sev=({alert_severity}[^=]+?)\s*\w+="""
    """policyName =({policy_name}[^=]+?)\s*\w+="""
    """cat=({category}[^=]+?)\s*\w+="""
    """fileSize=({bytes}\d+)"""
    """http_status=({http_response_code}\d+)"""
    """\sfileName =({file_name}.+?)\s*(\w+=|$)""",
    """ifdir=({direction}[^=]+?)\s*\w+="""
    """\Wifname=(|({src_interface}.+?))(\s+\w+=|\s*$)"""
    """\surl=({url}.+?)\s+\w+="""
  ]


}
```