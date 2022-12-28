#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-dlpincident
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """| app=symantec:dlp:incident""","""| Manager_Email=""" ]
  Fields = [
    """incident_id="({alert_id}\d+)"""",
    """\|\spolicy="({alert_name}[^"]+)"""",
    """\|\sseverity="({alert_severity}[^"]+)"""",
    """\|\sprotocol="({alert_type}[^"]+)"""",
    """\|\incident_type="({alert_type}[^"]+)""",
    """\|\ssender="(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({os}\w+):\/+({domain}[^\/]+)\/({user}[^"]+))"""",
    """\|\sprotocol="({protocol}[^"]+)"""",
    """\|\srecipient="(((({account}[^@]+)@)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)|(N/A|(?i)Unknown|({target}[^"]+)))"""",
    """\|\sBusiness_Unit="({additional_info}[^"]+)"""",
    """\|\sRR_Action="({action}[^"]+)""",
    """\|\smatch_count="({match_count}\d+)""",
    """\|\sfilename="(N/A|({file_path}({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\\/"]+?)))\s*"""",
    """\|\sEP_Machine="({src_host}[^"]+)""",
    """\|\sEP_IP="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "protocol->dlpProtocol", "src_ip->dlpDeviceName",  "alert_type->dlpActionTaken"]
    NameTemplate = """Vontu DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]

}
```