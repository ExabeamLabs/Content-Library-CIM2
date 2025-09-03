#### Parser Content
```Java
{
Name = "bitglass-casb-json-file-read-success-download"
  Conditions = [
    """"activity":"""
    """, Downloaded"""
    """ api.bitglass.com """ 
  ]
  ParserVersion = "v1.0.0"

bitglass-json-activity = {
    Vendor = "Bitglass"
    Product = "Bitglass CASB"
    ExtractionType = json
    TimeFormat = "dd MMM yyyy HH:mm:ss"
    Fields = [
      """exa_json_path=$.time,exa_field_name=time""",
      """exa_json_path=$.instancename,exa_field_name=host""",
      """exa_json_path=$.user,exa_regex=\s*"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))"""",
      """exa_json_path=$.email,exa_regex=\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
      """exa_json_path=$.device,exa_field_name=os""",
      """exa_json_path=$.application,exa_field_name=app""",
      """exa_json_path=$.ipaddress,exa_regex=\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """exa_json_path=$.filename,exa_regex=\s*"({src_file_name}[^"]+?(\.({file_ext}[^."]+))?)",""",
      """exa_json_path=$.activity,exa_field_name=access""",
      """exa_json_path=$.useragent,exa_field_name=user_agent""",
      """exa_json_path=$.url,exa_field_name=file_url"""
    ]
    DupFields = [ "src_file_name->file_name" 
}
```