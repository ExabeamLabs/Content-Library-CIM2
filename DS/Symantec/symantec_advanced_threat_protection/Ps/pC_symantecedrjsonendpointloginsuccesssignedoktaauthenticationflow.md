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
    Product = Symantec Advanced Threat Protection
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """\\"time\\":\\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """\\"message\\":\\"({additional_info}[^"\\]+)""",
      """\\"user_name\\":\\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """\\"event_id\\":({event_code}\d+)""",
      """\\"user_uid\\":\\"({user_id}[^\\"]+)""",
      """\\"destinationServiceName\\":\\"({app}[^\\"]+)""",
      """\\"session_uid\\":\\"({session_id}[^\\"]+)""",
      """\\"ipv4\\":\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\\"device_os_name\\":\\"({os}[^"\\]+)""",
      """\\"device_name\\":\\"({host}[\w\-.]+)""",
      """\\"device_domain\\":\\"({domain}[^"\\]+)"""
    
}
```