#### Parser Content
```Java
{
Name = cynet-cynetedr-cef-alert-trigger-success-endpointalert
  Vendor = Cynet
  Product = Cynet EDR
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions = [ """CEF:""", """|Cynet|""", """sev=""" , """cat=END-POINT Alert""" ]
  ParserVersion = v1.0.0
  Fields = [
    """\WrtUtc=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d.\d\d\d)""",
    """\Wdhost=({dest_host}[\w\-.]+)""",
    """\Wduser=(({domain}[^\\\/=]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\|Cynet\|([^\|]*\|){3}({alert_name}[^\|]+)""",
    """\Wsev=({alert_severity}\w+)""",
    """\Wcat=({alert_type}[^=]+?)\s*(\w+=|\$)""",
    """\|Cynet\|([^\|]*\|){4}({risk_level}\d+)""",
    """\WetwAlertId=({alert_subject}[^=]+?)\s*(\w+=|\$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WosVer=({os}[^=]+?)\s*(\w+=|\$)""",
    """\WfileHash=({hash_md5}[^\s]+)""",
    """\WfilePath=({file_path}[^=]+?)\s*(\w+=|\$)""",
    """\Wfname=({file_name}[^=]+?)\s*(\w+=|\$)""",
    """\WppParams=({additional_info}[^=]+?)\s*(\w+=|\$)""",
    """\WpParams=({command}.+?)\s*(\w+=|\$)"""
  ]


}
```