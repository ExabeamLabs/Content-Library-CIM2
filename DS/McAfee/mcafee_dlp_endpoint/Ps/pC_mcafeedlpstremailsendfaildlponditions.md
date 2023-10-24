#### Parser Content
```Java
{
Name = mcafee-dlp-str-email-send-fail-dlponditions
      Vendor = McAfee
      Product = McAfee DLP Endpoint
      TimeFormat = "MM/dd/yyyy HH:mm:ss a"
      Conditions = [ """<McAfee DLP Conditions>""" ]
      Fields = [
        """([^\|]*\|){0}"?({alert_id}\d+)(\||")""",
        """(".*?"\||[^|]*\|){1}"({email_subject}[^"]+)"\|""",
        """(".*?"\||[^|]*\|){4}"?({alert_name}[^"]+)(\||")""",
        """(".*?"\||[^|]*\|){4}"?({alert_type}[^"]+)(\||")""",
        """(".*?"\||[^|]*\|){1}"({alert_type}[^"]+)"\|\d+\|\d+\|"WEB""",
        """(".*?"\||[^|]*\|){5}"?({time}\d+\/\d+\/\d+ \d+:\d+:\d+ (AM|am|PM|pm))""",
        """(".*?"\||[^|]*\|){8}"?({src_email_address}[^"]+)(\||")""",
        """(".*?"\||[^|]*\|){10}"({email_recipients}[^"]+)"""",
        """(".*?"\||[^|]*\|){10}"({target}[^"]+)"""",
        """(".*?"\||[^|]*\|){10}"'?({external_address}[^@]+@[^'",]+)""",
        """(".*?"\||[^|]*\|){6}"?({alert_severity}\d+)(\||")""",
        """(".*?"\||[^|]*\|){11}"?({domain}[^"\\\/]+)?[\\\/]*({user}[\w\.\-]{1,40}\$?)(\||")"""
      ]
      DupFields = [ "src_email_address->email_user" ]
	  ParserVersion = "v1.0.0"
    

}
```