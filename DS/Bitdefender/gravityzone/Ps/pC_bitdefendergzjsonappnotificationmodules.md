#### Parser Content
```Java
{
Name = "bitdefender-gz-json-app-notification-modules"
   Vendor = "Bitdefender"
   Product = "GravityZone"
   ParserVersion = "v1.0.0"
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """gravityzone:""", """"module":"modules"""" ]
   Fields = [
      """"computer_name":"({src_host}[^"]+)""",
      """"computer_fqdn":"({src_domain}[^"]+)""",
      """"computer_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# computer_id is removed
# malware_status is removed
# aph_status is removed
# avc_status is removed
# uc_web_filtering is removed
# uc_categ_filtering is removed
# uc_application_status is removed
# dp_status is removed
# pu_status is removed
# dlp_status is removed
# pu_status is removed
  ]


}
```