#### Parser Content
```Java
{
Name = "juniper-srx-cef-alert-trigger-success-inpolicy"
Vendor = "Juniper Networks"
Product = "Juniper SRX Series"
TimeFormat = "epoch_sec"
Conditions = [
  """: IDP_ATTACK_LOG_EVENT: IDP: """
  """ protocol and service """
  """ in policy """
]
Fields = [
  """ ({host}[^\s]+) [^\s]+: IDP_ATTACK_LOG_EVENT: """
  """: IDP_ATTACK_LOG_EVENT: IDP: at ({time}\d{10})"""
  """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)\W+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)"""
  """ for ({protocol}[^\s]+) protocol and service ({service_name}[^\s]+) application ({app}[^\s]+) by rule ({rule_id}[^\s]+)"""
  """attack:.+?action=(NONE|({result}[^\s,]+))"""
  """attack:.+?threat-severity=({alert_severity}[^\s,]+)"""
  """attack:.+?username=(N\/A|({user}[\w\.\-]{1,40}\$?))"""
  """\sname=({alert_name}[^,\s]+)"""
]
ParserVersion = "v1.0.0"


}
```