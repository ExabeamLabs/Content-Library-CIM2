#### Parser Content
```Java
{
Name = inky-ap-json-alert-trigger-success-inkyevent
  ParserVersion = v1.0.0
  Vendor = Inky
  Product = Inky Anti-Phishing
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Conditions = [ """"inky_analysis":""", """"threat_level":""", """"identifier":"inky-event"""", """"message_id":""" ]
  Fields = [
     """"reason_htmls":\s*\["({additional_info}[^\]]+?)(",|"\])""",
     """"reason_titles":\s*\["({alert_name}[^"]+)""",
     """"result_bucket":\s*"({alert_severity}[^"]+)"""",
     """"short_reasons":\s*\s*\["({alert_type}[^"]+)""",
     """"client_ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
     """\d\d:\d\d:\d\d\.\S+\s({host}[^\s]+)\s+inky""",
     """"rcpt_to_addresses":\s*\["({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
     """"mail_from":\s*"<?({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>?"""",
     """"email_address_IP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"subject":\s*"({email_subject}[^"]+?)\s*"""",
     """"internaldate_utc_seconds":\s*({time}\d{10})""",
     """"original_url":\s*"({malware_url}[^"]+)"""",
     """"tracking_id":({alert_id}\d+)""",
     """"threat_level":({threat_level}\d+)""",
     """"sender_IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
     """exa_json_path=$.data.inky_analysis.suspicious_details.reason_htmls,exa_regex=\["({additional_info}[^\]]+?)(",|"\])"""
     """exa_json_path=$.data.inky_analysis.suspicious_details.reason_titles,exa_regex=\s*\["({alert_name}[^"]+)""",
     """exa_json_path=$.data.inky_analysis.suspicious_details.result_bucket,exa_field_name=alert_severity"""
     """exa_json_path=$.data.meta_data.sender_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
     """exa_json_path=$.data.meta_data.rcpt_to_addresses,exa_regex=\[\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
     """exa_json_path=$.data.meta_data.mail_from,exa_regex=<?({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>?""",
     """exa_regex="rcpt_to_addresses":\s*\["({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
     """exa_json_path=$.data.meta_data.subject,exa_field_name=email_subject"""
     """exa_json_path=$.data.meta_data.internaldate_utc_seconds,exa_field_name=time"""
     """exa_json_path=$.data.inky_analysis.suspicious_details.threat_level,exa_field_name=threat_level"""
  ]
  DupFields = ["dest_email_address->email_address"]


}
```