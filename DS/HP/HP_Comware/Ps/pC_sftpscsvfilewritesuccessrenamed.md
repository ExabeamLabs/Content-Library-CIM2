#### Parser Content
```Java
{
Name = sftp-s-csv-file-write-success-renamed
Conditions = [
  """ sftp-"""
  """"Renamed""""
]
ParserVersion = "v1.0.0"

f5-waf-activity.Fields} [
    """\(({user}[^\}\s]+)\) CMD""",
    """\sCMD \(\s*({process_command_line}[^\)]+)\)""",
    """\sCMD \(\s*[^\/]*?({process_path}({process_dir}\/[^\)]*?)({process_name}[^\/]*?[^\\]))((\\\\)*\s|\))"""
  ]
  ParserVersion = "v1.0.0"
},

  {
    Name = hp-comware-str-process-create-success-commandis
    Vendor = HP
	Product = HP Comware
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [ """-User=""", """-Task=""", """Source: /""", """TAG:""", """Command is""", """-IPAddr=""" ]
    Fields = [
      """({time}\w{3}\s+\d+\s+\d{2}:\d{2}:\d{2}\s+\d{4})\s+({host}[^\s]+)\s+%%""",
      """-User=({user}[^;]+);""",
      """-IPAddr=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """-DevIP=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """Command\s*is\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s*Source:""",
      """Command\s*is\s*({process_command_line}.+?)\s*Source:"""
    ]
    DupFields = [ "host->dest_host" ]
	ParserVersion = "v1.0.0"
  },

{
  Name = huawei-usg-kv-process-create-success-shell
  Vendor = Huawei
  Product = Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """SHELL/""", """ command=""", """ result=""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """\sip=({src_ip}[a-fA-F\d.:]+)""",
     """\suser=(({email_address}[^@,]+@[^@,]+)|({user}[^,]+))""",
     """\scommand=({process_command_line}({process_path}({process_dir}[^,]*?[\\\/]+)?({process_name}[^\\\/\s]+))[^,]*?),""",
     """\sresult=({result}\w+)""",
  ]
  ParserVersion = "v1.0.0"
},

${SentinelOneParsersTemplates.json-sentinelone-threat-events}{
  Name = sentinelone-singularity-json-process-create-success-processcreation
  Product = Singularity
  Conditions = [ """"eventType": "Process Creation"""",  """"agentName":""", """"processImagePath":""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-threat-events.Fields}[
    """"parentProcessName":\s*"({parent_process_name}[^"]+)"""",
    """"processImagePath":\s*"({process_path}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = dtexsystems-intercept-cef-process-create-success-processcreated
  Vendor = Dtex Systems
  Product = DTEX InTERCEPT
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Dtex|""", """|ProcessCreated|""" ]
  Fields = [
    """\Wstart=({time}\d+)""",
    """\|Dtex\|([^\|]*\|){2}(ProcessActivity\|)?({operation_type}[^\|]+)\|""",
    """\|Dtex\|([^\|]*\|){3}Running\s*({process_path}({process_dir}(?:[^\s\|]+)?[\\\/]+)?({process_name}[^\\\/\|]+))\|""",
    """\|Dtex\|([^\|]*\|){3}Running\s*({path}.+?)\|""",
    """\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)""",
    """"ProcessId":\s*"({process_id}\d+)"""",
    """\WProcess_Name =(?:\s*|({process_name}.+?)\s+)(\w+=|$)""",
    """\WUser_Name =(({domain}[^\\]+)\\+)?({user}[^\\\s]+)\s""",
    """\WProcess_Parameters="({path}({process_path}({process_dir}(?:[^"]+)?[\\\/]+)?({process_name}[^\\\/\)"]+)))""",
    """\Wreason=({process_command_line}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"
},

{
  Name = blackberry-protect-kv-alert-trigger-success-devicecontrol
  ParserVersion = v1.0.0
  Vendor = BlackBerry
  Product = BlackBerry Protect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """CylancePROTECT """, """Event Type: DeviceControl""", """Device Name:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})\d+""",
    """Event Type:\s*({alert_type}[^,]+)\s*,""",
    """Event Name:\s*({alert_name}[^,]+)\s*,""",
    """Device Name:\s*({src_host}[^,]+)\s*,""",
    """External Device Serial Number:\s*({device_id}[^,]+)\s*,""",
    """External Device Name:\s*({additional_info}[^,]+)\s*,""",
    """External Device Type:\s*({device_type}[^,]+)\s*,""",
  
}
```