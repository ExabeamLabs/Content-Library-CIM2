#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-113039
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Network Security
    TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Conditions = [ """-113039""", """%ASA-""" ]
    Fields = [
      """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
      """\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """({time}\w+\s+\d+\s+\d+\s+\d\d:\d\d:\d\d)""",
      """User\s+<((cn=({src_host}[^>,@]+))|({=src_host}[^.<@]+\.[^.>@]+\.[^>]*)|((({domain}[^\\\/>]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(>|,[^>]+?dc=({=domain}[^>,]+))""",
      """User\s+<({email_address}[^@>]+@[^@>]+)>""",
      """ IP <({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))>""",
      """ Group\s+<({realm}.+?)>""",
      """\sGroup\s*<({group_name}[^>]+)>"""
      """\sUser\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)>"""
      """\w{3}\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(\d+|({host}[\w\-\.]+))\s"""
      """\sUser\s*<({account}[\w\.\-\!\#\^\~]{1,40}\$?)>"""
    ]
  

}
```