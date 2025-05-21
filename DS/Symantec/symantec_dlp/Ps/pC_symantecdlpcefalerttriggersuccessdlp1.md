#### Parser Content
```Java
{
Name = symantec-dlp-cef-alert-trigger-success-dlp-1
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = ["MMMM dd, yyyy HH:mm:ss","MMM dd, yyyy hh:mm:ss a"]
    Conditions = [ """CEF""","""|Symantec|DLP|""","""Application_Name =""","""Sender=""" ]
    Fields = [
      """({host}[\w\-.]+)\s+CEF:""",
      """Occurred_On="({time}\w+\s\d{1,2},\s\d{4}\s\d{1,2}:\d{2}:\d{2}\s(AM|PM))""",
      """Occurred_On="({time}\w+\s\d{2},\s\d{4}\s\d{2}:\d{2}:\d{2}\sAM|PM)"""",
      """Recipients="({recipients}[^"]*?<?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)""",
      """Endpoint_Username="(({domain}[^"]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """Severity="({alert_severity}[^"]+)""",
      """Protocol="({protocol}[^"]+)""",
      """Sender="((?i)n\/a|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
      """Machine_IP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """Policy_Name ="({alert_name}[^"]+)""",
      """Incident_ID="({alert_id}[^"]+)""",
      """File_Name ="((?i)n\/a|({file_name}[^"]+?))""""
    ]
    DupFields = [
      "file_name->object"
    ]
	ParserVersion = v1.0.0


}
```