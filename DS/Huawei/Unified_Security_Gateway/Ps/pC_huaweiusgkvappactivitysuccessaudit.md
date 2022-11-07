#### Parser Content
```Java
{
Name = huawei-usg-kv-app-activity-success-audit
  ParserVersion = "v1.0.0"
  Conditions = [ """AUDIT/""", """%%""", """ AuditPolicy=""" ]
  Fields = ${HUAWEILMSParserTemplates.huawei-ids-2.Fields}[
    """%%[^:]*?:\s*({event_name}[^\.\(]+)""",
    """\sSrcIp=({src_ip}[a-fA-F\d.:]+)""",
    """\sDstIp=({dest_ip}[a-fA-F\d.:]+)""",
    """\sSrcPort=({src_port}\d+)""",
    """\sDstPort=({dest_port}\d+)""",
    """\sUser="(?!\d+\.\d+\.\d+\.\d+)(?:unknown|({email_address}[^@"]+@[^@"]+)|({user}[^"]+))"""",
    """\sProtocol=({protocol}[^,]+)""",
    """\sApplication="({app}[^"]+)""",
# audit_type is removed
    """\sDirection=({direction}[^,]+)""",
    """\sURL="({url}[^"]+)""",
    """\sFileSize=({bytes}\d+)""",
  ]

huawei-ids-2 {
  Vendor = Huawei
  Product = Unified Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
     """:\d\d\s({host}[^\s]+)\s*%""",
     """PeerAddress=({dest_ip}[^,]+)""",
     """PeerPort=({dest_port}\d+)""",
     """Reason=({policy_name}[^)]+)""",
     """:\s*({event_name}[^:\/]+)\.\s*\(""",
     """Destination address:\s*({dest_ip}[^,]+)"""
  
}
```