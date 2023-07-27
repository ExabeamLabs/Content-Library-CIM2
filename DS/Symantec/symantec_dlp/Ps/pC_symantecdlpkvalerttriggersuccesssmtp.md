#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-smtp
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """| app=symantec:dlp:incident""","""| protocol="SMTP"|""" ]
  Fields = [
    """incident_id="({alert_id}\d+)"""",
    """\|\spolicy="({alert_name}[^"]+)"""",
    """\|\sseverity="({alert_severity}[^"]+)"""",
    """\|\spolicy_rule="({policy_name}[^"]+?)\s*"""",
    """\|\spolicy="[^"]+\-\s*({alert_type}[^"]+)""",
    """\|\sUserID="({user}[\w\.\-]{1,40}\$?)"""",
    """\|\ssender="({src_email_address}[^"]+)"""",
    """\|\ssubject="\s*(N/A|({email_subject}[^"]+?))\s*"""",
    """\|\sprotocol="({protocol}[^"]+)"""",
    """\|\srecipient="({email_recipients}[^"]+)"""",
    """\|\srecipient="({external_address}[^,"]+)""",
    """\|\sBusiness_Unit="({additional_info}[^"]+)"""",
    """\|\sfilename="(N/A|(?i)unknown|({target}[^"]+?))\s*"""",
    """\|\sfilename="(N/A|(?i)unknown|({file_name}[^"]+?\.\w+))""",
    """\|\sRR_Action="({action}[^"]+)""",
    """\|\smatch_count="({match_count}\d+)""",
    """\|\sEP_Machine="({src_host}[^"]+)""",
    """\|\sEP_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```