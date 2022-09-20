#### Parser Content
```Java
{
Name = microsoft-defenderep-json-dll-load-imageloadevents
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender for Endpoint"
  Conditions = [  """"Type":"AdvancedHuntingDeviceImageLoadEvents_CL""", """TenantId""", """TimeGenerated""", """ProcessAccountName_s""" ]
  Fields = ${DLMicrosoftParsersTemplates.defender-atp-events.Fields}[
     """"FileName"+:\s*"+({object}[^"]+)"""
     """DeviceName"+:\s*"+({dest_host}[^"]+)""",
]

defender-atp-events = {
    Vendor = Microsoft
    Product = Defender ATP
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"DeviceName":"({host}[^"]+)""""
      """"LogonType":"({login_type_text}[^"]+)"""",
      """"AccountName":"({user}[^"]+)"""",
      """"AccountDomain":"({domain}[^"]+)"""",
      """"InitiatingProcessFileName":"({process_name}[^"]+)"""",
      """"category":"({event_name}[^"]+)"""",
      """"ActionType":"({action}[^"]+)"""",
      """"RemoteIP":"({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
      """"Protocol":"({protocol}[^"]+)""""
    ]
    DupFields = ["host->dest_host"
}
```