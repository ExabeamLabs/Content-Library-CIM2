#### Parser Content
```Java
{
Name = symantec-edr-json-app-logout-success-signedoutcloudconsol
  ParserVersion = "v1.0.0"
  Conditions = [ """signed out from the cloud console""" ,"""Symantec"""]
  Fields = ${DLSymantecParserTemplates.symantec-system-info-template.Fields}[
    """({event_name}signed out)""",
  ]

symantec-system-info-template = {
    Vendor = Symantec
    Product = Symantec Advanced Threat Protection
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """(\\)?"time(\\)?":(\\)?"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """\\"message\\":\\"({additional_info}.+?)\\",\\"\w+\\":""",
      """(\\)?"user_name(\\)?":(\\)?"({user}[^\\"]+)""",
      """(\\)?"event_id(\\)?":({event_code}\d+)""",
      """(\\)?"user_uid(\\)?":(\\)?"({user_uid}[^\\"]+)""",
      """(\\)?"destinationServiceName(\\)?":(\\)?"({app}[^\\"]+)""",
      """(\\)?"session_uid(\\)?":(\\)?"({session_id}[^\\"]+)""",
      """(\\)?"ipv4(\\)?":(\\)?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """(\\)?"device_os_name(\\)?":(\\)?"({os}[^"\\]+)""",
      """(\\)?"device_name(\\)?":(\\)?"({host}[\w\-.]+)""",
      """(\\)?"device_domain(\\)?":(\\)?"({domain}[^"\\]+)"""
    
}
```