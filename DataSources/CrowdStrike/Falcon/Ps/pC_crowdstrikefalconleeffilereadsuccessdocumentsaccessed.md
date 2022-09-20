#### Parser Content
```Java
{
Name = crowdstrike-falcon-leef-file-read-success-documentsaccessed
  ParserVersion = v1.0.0  
  Product = Falcon
  Conditions = [ """LEEF:""", """|CrowdStrike|FalconHost|""", """cat=DocumentsAccessed""" ]
  Fields = ${CrowdStrikeParsersTemplates.leef-crowdstrike-alert-t.Fields} [
    """CrowdStrike\|([^|]+\|){2}({alert_name}[^|]+)""",
    """\WdocAccessedFileName =({file_name}[^|"]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\WdocAccessedFilePath=({file_dir}[^=]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\Wdescription=({additional_info}[^=]+?)\s*(\||\w+=|$|"+\s*$)"""
  ]

leef-crowdstrike-alert-t = {
    Vendor = CrowdStrike
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\WdevTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
      """\Wduser=(?!N\/A)({user}[^=@]+?)(@({email_domain}[^@]+?))?(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
      """\WusrName =(?!N\/A)({user}[^=@]+?)(@({email_domain}[^@]+?))?(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
      """\Wdomain=(?!N\/A)({web_domain}[^=]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)""",
      """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\Wdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
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