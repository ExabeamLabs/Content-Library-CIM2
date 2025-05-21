#### Parser Content
```Java
{
Name = crowdstrike-falcon-leef-file-write-success-executableswritten
  ParserVersion = v1.0.0 
  Product = Falcon
  Conditions = [ """LEEF:""", """|CrowdStrike|FalconHost|""", """cat=ExecutablesWritten""" ]
  Fields = ${CrowdStrikeParsersTemplates.leef-crowdstrike-alert-t.Fields} [
    """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\WexeWrittenFileName =({file_name}[^|"]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
    """\WexeWrittenFilePath=({file_path}[^=]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
  ]

leef-crowdstrike-alert-t = {
    Vendor = CrowdStrike
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\WdevTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
      """\Wduser=(?!N\/A)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
      """\WusrName =(?!N\/A)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
      """\Wdomain=(?!N\/A)({domain}[^=]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\WsrcPort=({src_port}\d+)""",
      """\WdstPort=({dest_port}\d+)""",
      """\Wcat=({category}[^\|]+?)\s*(\||\w+=|$|"+\s*$)""",
      """\Wproto=({protocol}[^\s]+?)\s*(\||\w+=|$|"+\s*$)""",
      """\WfileName =({src_file_name}.+?)\s*(\||\w+=|$|"+\s*$)""",
      """\Wresource=({src_host}.+?)\s*(\||\w+=|$|"+\s*$)""",
      """\Wsev=({alert_severity}.+?)\s*(\||\w+=|$|"+\s*$)""",
      """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
      """\Wurl=({additional_info}[^\|]+?)\s*(\||\w+=|$|"+\s*$)""",
      """\Wmd5=({hash_md5}[^\s]+?)\s*(\||\w+=|$|"+\s*$)""",
      """({app}FalconHost)"""
    ]
  DupFields = [ "category->alert_type" 
}
```