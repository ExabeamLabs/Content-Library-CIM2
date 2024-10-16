#### Parser Content
```Java
{
Name = symantec-dlp-str-alert-trigger-success-blocked
	  ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ PROTOCOL """, """ POLICY """, """ MATCHES """, """ SEVERITY """, """ BLOCKED """, """ URL """, """ SENDER """, """ RECIPIENTS """, """ FILE_NAME """, """ PARENT_PATH """ ]
    Fields = [
    """\sFILE_NAME\s(?:N\/A|({email_attachments}({file_name}.+?)))\sPARENT_PATH\s""",
    """\sSENDER\s\w+:\/\/({domain}[^\<\>\[\]\"\/\\:;\|=,+*\?]+)\/({user}[\w\.\-\!\#\^\~]{1,40}\$?)\sRECIPIENTS\s""",
    """\sSENDER\s({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\sRECIPIENTS\s""",
    """\sSENDER\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\sRECIPIENTS\s""",
    """\sBLOCKED\s(?:N\/A|({action}.+?))\sURL\s""",
    """\sSEVERITY\s(?:N\/A|({alert_severity}.*?))\sBLOCKED\s""",
    """\sINCIDENT\s(?:N\/A|({alert_id}\d{1,100}?))\sPOLICY\s""",
    """\sPOLICY\s(?:N\/A|({alert_type}.+?))\sMATCHES\s""",
    """\sPROTOCOL\s(?:N\/A|({protocol}.+?))\sINCIDENT\s""",
    """\sRECIPIENTS\s({target}(http:\/\/|https:\/\/).+?)\/.*?\sFILE_NAME\s""",
    """\sRECIPIENTS\s(?:N\/A|https:\/\/.+?|http:\/\/.+?|Unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))[\s\,]""",
    """\sRECIPIENTS\s(?:N\/A|https:\/\/.+?|http:\/\/.+?|Unknown|({email_recipients}.+?))\s""",
    ]
    DupFields = [ "alert_type->alert_name" ]
  

}
```