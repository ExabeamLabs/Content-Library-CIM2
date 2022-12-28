#### Parser Content
```Java
{
Name = symantec-edr-json-endpoint-login-success-signedoktaauthenticationflow
  ParserVersion = "v1.0.0"
  Conditions = [ """signed in to the console using Broadcom OKTA authentication flow""","""\"event_id\":20001""" ]
  Fields = ${SymantecParsersTemplates.symantec-app-template.Fields}[
    """({event_name}signed in)""",
  ]

symantec-app-template = {
    Vendor = Symantec
    Product = Symantec EDR
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """\\"time\\":\\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """\\"message\\":\\"({additional_info}[^"\\]+)""",
      """\\"user_name\\":\\"({user}[^\\"]+)""",
      """\\"event_id\\":({event_code}\d+)""",
      """\\"user_uid\\":\\"({user_id}[^\\"]+)""",
      """\\"destinationServiceName\\":\\"({app}[^\\"]+)""",
      """\\"session_uid\\":\\"({session_id}[^\\"]+)""",
      """\\"ipv4\\":\\"({src_ip}[A-Fa-f\d:.]+)""",
      """\\"device_os_name\\":\\"({os}[^"\\]+)""",
      """\\"device_name\\":\\"({host}[\w\-.]+)""",
      """\\"device_domain\\":\\"({domain}[^"\\]+)"""
    
}
```