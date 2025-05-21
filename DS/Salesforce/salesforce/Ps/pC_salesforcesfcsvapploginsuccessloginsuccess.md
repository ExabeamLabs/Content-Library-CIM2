#### Parser Content
```Java
{
Name = salesforce-sf-csv-app-login-success-loginsuccess
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "MM/dd/yyyy hh:mm a"
  Conditions = [ ""","Success"""", ""","login.salesforce.com""" ]
  Fields = [
    """([^,]*,){0}"({email_address}[^@]+@({email_domain}[^\s",]+))",""",
    """([^,]*,){1}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?",""",
    """([^,]*,){2}"({time}\d+\/\d+\/\d+ \d+:\d+ (AM|PM|am|pm))""",
    """([^,]*,){4}"({result}[^"]+)",""",
    """([^,]*,){5}"({browser}[^"]+)",""",
    """([^,]*,){6}"({dest_host}[^"]+)""",
    """({app}salesforce)"""
  ]


}
```