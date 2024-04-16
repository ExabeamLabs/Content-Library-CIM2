#### Parser Content
```Java
{
Name = mcafee-solidifier-kv-alert-trigger-success-signatureid
    Vendor = McAfee
    Product = McAfee Application Control
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [ """Solidifier""" , """signature=""" , """category=""", """timestamp=""", """signature_id"""]
    Fields = [
      """\stimestamp="*({time}[^"]+)""",
      """signature="*({alert_name}[^"]+)""",
      """signature_id="*({signature_id}[^"]+)""",
      """category="*({threat_category}[^"]+)""",
      """severity_id="*({alert_severity}\d+)""",
      """event_description="*({additional_info}[^"]+)""",
      """threat_type="*(?:none|({alert_type}[^"]+))""",
      """file_name="*({file_dir}[^"]+[\\\/]+)?({file_name}[^"]+)"""",
      """src_ip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """dest_ip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\suser="*(?:N\/A|({user}[\w\.\-]{1,40}\$?))""",
      """dest_nt_domain="*({domain}[^"]+)""",
      """os="*({os}[^"]+)""",
      """vendor_action="*(?:none|({action}[^"]+))""",
      """AutoID="*({alert_id}[^"]+)""",
    ]
    ParserVersion = "v1.0.0"


}
```