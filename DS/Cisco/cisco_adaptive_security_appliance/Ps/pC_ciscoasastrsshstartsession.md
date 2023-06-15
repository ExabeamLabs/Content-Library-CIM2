#### Parser Content
```Java
{
Name = cisco-asa-str-ssh-start-session
  ParserVersion = "v1.0.0"
  Conditions = [
"""%SSH-"""
"""SSH2_SESSION:"""
]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
    """SSH2_SESSION:\s({event_name}SSH2 Session request) from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+? for user '(|({user}[^\s']+))"""
    """({result}Succeeded|Failed)"""
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```