#### Parser Content
```Java
{
Name = cisco-asa-str-ssh-close-ssh
  ParserVersion = "v1.0.0"
  Conditions = [ 
"""%SSH-"""
"""SSH2_CLOSE:""" 
]
  Fields = ${CiscoParsersTemplates.cisco-system-info-aa.Fields} [
    """SSH2_CLOSE:\sSSH2 Session from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+? for user '(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """({result}closed)"""
  ]

cisco-system-info-aa = {
  Vendor = "Cisco"
  Product = Cisco Network Infrastructure and Management
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec","epoch", "MMM dd HH:mm:ss", "MMM dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy MMM dd HH:mm:ss.SSSSSS"]
  Fields = [
    """(\d+:\s*({host}[\w\-\.]+)\s*(:\s*\d+)?:\s*)?\w+\s\d+\s(\d\d\d\d\s)?\d\d:\d\d:\d\d(\.\d+)?(\s\w+)?:\s*%"""
    """\w+\s\d+\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)\s"""
    """\s({time}\w+ \d+(\s*\d+)? \d+:\d+:\d+(\.\d+)?)"""
    """({time}\d+ \w+ \d+ \d+:\d+:\d+(\.\d+)?)\s+\w+:\s+\%""",
    """\Wrt=({time}\d{13})""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```