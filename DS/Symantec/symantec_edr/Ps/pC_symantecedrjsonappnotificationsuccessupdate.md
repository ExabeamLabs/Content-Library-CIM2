#### Parser Content
```Java
{
Name = symantec-edr-json-app-notification-success-update
  ParserVersion = "v1.0.0"
  Conditions = [ """"An update for ""","""Content was downloaded from ""","""Symantec""" ]
  Fields = ${DLSymantecParserTemplates.symantec-system-info-template.Fields}[
    """({event_name}update for)""",
  ]


symantec-system-info-template = {
    Vendor = Symantec
    Product = Symantec EDR
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """\\"time\\":\\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """\\"message\\":\\"({additional_info}.+?)\\",\\"\w+\\":""",
      """\\"user_name\\":\\"({user}[^\\"]+)""",
      """\\"event_id\\":({event_code}\d+)""",
      """\\"user_uid\\":\\"({user_uid}[^\\"]+)""",
      """\\"destinationServiceName\\":\\"({app}[^\\"]+)""",
      """\\"session_uid\\":\\"({session_id}[^\\"]+)""",
      """\\"ipv4\\":\\"({src_ip}[A-Fa-f\d:.]+)""",
      """\\"device_os_name\\":\\"({os}[^"\\]+)""",
      """\\"device_name\\":\\"({host}[\w\-.]+)""",
      """\\"device_domain\\":\\"({domain}[^"\\]+)"""
    
}
```