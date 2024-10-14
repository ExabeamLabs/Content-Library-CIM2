#### Parser Content
```Java
{
Name = zscaler-ia-csv-app-activity-success-nssdelete
  ParserVersion = "v1.0.0"
  Conditions = [ """zscaler""", """NSS""", ""","ZIA",""", ""","DELETE",""", ""","SUCCESS","""]
 
zscaler-ia-csv-events = {
  Vendor = Zscaler
  Product = Zscaler Internet Access 
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """\w{3}\s+({time}\w{3}\s+\d{2}\s+(\d{2}:){2}\d{2}\s+\d{4})""",
    """"({app}ZIA)"""",
    """\d{2}:\d{2}:\d{2}\s+\d{4}",("[^"]+",)"({operation}[^"]+)",("[^"]+",)"({object}[^"]+)","({resource}[^"]+)","({app_type}[^"]+)","(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))","(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)","({result}[^"]+)"""",
    """"ZIA","({additional_info}.*)}""""
  
}
```