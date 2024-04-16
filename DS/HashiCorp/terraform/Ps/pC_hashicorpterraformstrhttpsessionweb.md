#### Parser Content
```Java
{
Name = "hashicorp-terraform-str-http-session-web"
 Vendor = "HashiCorp"
 Product = "Terraform"
 TimeFormat = "yyyy/MM/dd HH:mm:ss"
 Conditions = [
   """ TFCS_LOG """
 ]
 Fields = [
   """\s({host}[\w\-.]+)\s+TFCS_LOG\s+.*?({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)\s+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+)):({src_port}\d+)""",
   """\s({host}[\w\-.]+)\s+TFCS_LOG\s+.*?({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\s+({email_address}[^\s@]+@[^\s@]+)\s+({http_response_code}\d+)\s+({bytes}\d+)\s+({method}\S+)\s+(-|({url}(({protocol}[^:\\\/\s,\"]+):[\\\/]+)?[\\\/]*(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\\\/\s:,\"]+))(:({dest_port}\d+))?({uri_path}\/[^\s\?\",]*)?({uri_query}\?[^\"\s]*)?))\s+({action}[^\s]+)\s"""
 ]
 DupFields = [
   "action->resource"
 ]
 ParserVersion = "v1.0.0"


}
```