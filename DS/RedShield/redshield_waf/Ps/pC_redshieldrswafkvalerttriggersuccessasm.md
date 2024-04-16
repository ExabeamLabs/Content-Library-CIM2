#### Parser Content
```Java
{
Name = redshield-rswaf-kv-alert-trigger-success-asm
  Vendor = RedShield
  Product = RedShield WAF
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ASM:SUPPORT_ID=""", """TYPE=""", """DEST_IP=""", """DEST_PORT=""" ]
  Fields = [
    """;HOST=({host}[\w\-\.]+)"""
    """ASM:SUPPORT_ID=({incident_id}\d+)"""
    """;TYPE=({alert_name}[^=;]+)"""
    """;DATE=({time}[^=;]+)"""
    """;DEST_IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """;DEST_PORT=({dest_port}\d+);"""
    """;VIOLATION_DETAILS=({additional_info}.+?);VIOLATIONS="""
    """;IP_CLIENT=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """;METHOD=({method}[^;]+)"""
    """;USERNAME=(N\/A|({user}[^;]+))"""
    """;POLICY=({policy_name}[^;]+)"""
    """;PROTO=({protocol}[^;]+)"""
    """;REQ_STATUS=({status}[^;]+)"""
    """;RESP_CODE=({result_code}[^;]+)"""
    """;SEV=({alert_severity}[^;]+)"""
    """;SRC_PORT=({src_port}\d+)"""
    """;URI=({uri}[^=;]+)"""
  ]
  
  DupFields = ["alert_name -> alert_type"]


}
```