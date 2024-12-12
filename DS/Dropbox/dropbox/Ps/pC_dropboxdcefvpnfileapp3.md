#### Parser Content
```Java
{
Name = dropbox-d-cef-vpnfileapp-3
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =Dropbox""", """.tag""",  """"sharing"}""" ]
  Fields = ${DropboxParsersTemplates.cef-dropbox-activity.Fields}[
    """"assets":\s*\[[^\]]*?"display_name":\s*"({object}[^",]+)"""",
    """"assets":\[[^\]]+?".tag":"({file_type}folder)"[^\]]+?"display_name":"({folder_name}[^"]+)"""",
    """"assets":\[[^\]]+?".tag":"({file_type}file)"[^\]]+?"display_name":"({file_name}[^"]+)""""
  ]

cef-dropbox-activity = {
  Vendor = Dropbox
  Product = Dropbox
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d ({host}[\w\-.]+) \d+ \d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ""",
    """"timestamp":\s*"({time}[^"]+)""",
    """"host_name":\s*"({host}[^"]+)""",
    """"actor":\s*[^\}]*?"display_name":\s*"(?:N\/A|({full_name}[^"@]+))"""",
    """"actor":\s*[^\}]*?"email":\s*"(?:N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
    """"event_type":\s*"({operation}[^"]+)"""",
    """"event_type":\s*\{("description":\s*"[^"]+",\s*)?"\.tag":\s*"({operation}[^"]+)"""",
    """"description":\s*"({additional_info}[^"]+)"""",
    """"ip_address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({app}Dropbox)""",
    """"participants":\[\{"\.tag":"user","user":\s*[^\}]*?"display_name":"(?:N\/A|({dest_user_full_name}[^"@]+))","""
    """"participants":\[\{"\.tag":"user","user":\s*[^\}]*?"email":"(?:N\/A|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""""
  
}
```