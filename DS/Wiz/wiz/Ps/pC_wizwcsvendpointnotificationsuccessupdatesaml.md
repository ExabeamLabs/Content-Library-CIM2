#### Parser Content
```Java
{
Name = wiz-w-csv-endpoint-notification-success-updatesaml
 ParserVersion = "v1.0.0"
 Conditions = [ """,UpdateSAMLIdentityProvider,""", """,USER_ACCOUNT,""", """"loginURL"""" ]
 Fields = ${WizParserTemplates.wiz-system-info-events.Fields}[
   """({event_name}UpdateSAMLIdentityProvider)"""
   ]

wiz-system-info-events = {
  Vendor = Wiz
  Product = Wiz
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSZ"]
  Fields = [
   """ACCOUNT,({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)""",
   """\d\d:\d\d\.[^,]+,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"?({user_agent}[^"]*)"?,({result}\S+)""",
   
}
```