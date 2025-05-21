#### Parser Content
```Java
{
Name = unix-unix-json-endpoint-login-fail-sshd
  Product = Unix
  Conditions = [ """"ident":"sshd""", """nvalid user""" ]
  Fields = ${UnixParsersTemplates.unix-activity-json.Fields}[
    """exa_json_path=$.jsonPayload.message,exa_regex=(I|i)nvalid user (({domain}[^\\:]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.jsonPayload.message,exa_regex=from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.jsonPayload.message,exa_regex=\s+from\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"

unix-activity-json = {
    Vendor = Unix
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """exa_json_path=$.jsonPayload.host,exa_field_name=host""",
      """exa_json_path=$.jsonPayload.ident,exa_field_name=event_code""",
      """exa_json_path=$.jsonPayload.pid,exa_field_name=process_id""",
      """exa_json_path=$.timestamp,exa_field_name=time""",
    
}
```