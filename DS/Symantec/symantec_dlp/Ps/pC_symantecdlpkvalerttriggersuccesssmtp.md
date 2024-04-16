#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-smtp
  ParserVersion = v1.0.0
  Conditions = [ """| incident_type="email"|""","""| protocol="SMTP"|""" ]
  Fields = ${SymantecParsersTemplates.symantec-dlp-alert.Fields} [
    """\|\ssender="({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """\|\ssubject="\s*(N/A|({email_subject}[^"]+?))\s*"""",
    """\|\srecipient="(N/A|({email_recipients}[^"]+))""""
    """\|\srecipient="({external_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]

symantec-dlp-alert = {
      Vendor = Symantec
      Product = Symantec DLP
      TimeFormat = ["MMMM dd, yyyy HH:mm:ss a","yyyy-MM-dd HH:mm:ss"]
      Fields = [
        """incident_id="({alert_id}\d+)"""",
        """\|\spolicy="({alert_name}[^"]+)"""",
        """\|\sseverity=\s*"({alert_severity}[^"]+)"""",
        """\|\spolicy_rule="({policy_name}[^"]+?)\s*"""",
        """\|\incident_type="({alert_type}[^"]+)""",
        """\|\sUserID="({user}[\w\.\-]{1,40}\$?)"""",
        """\|\sprotocol="({protocol}[^"]+)"""",
        """\|\sBusiness_Unit="({additional_info}[^"]+)"""",
        """\|\sfilename="(N/A|(?i)unknown|({target}[^"]+?))\s*"""",
        """\|\sfilename="(N/A|(?i)unknown|({file_name}[^"]+?\.\w+))""",
        """\|\sRR_Action="({action}[^"]+)""",
        """\|\smatch_count="({match_count}\d+)""",
        """\|\sEP_Machine="({src_host}[^"]+)""",
        """\|\sEP_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
        """\|\sEP_Location="({src_location}[^"]+)""",
        """\|\application="({app}[^"]+)"""",
        """\|\device_id="({device_id}[^"]+)"""",
      ]
    
}
```