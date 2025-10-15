#### Parser Content
```Java
{
Name = amazon-awscloudtrail-cef-bucket-permission-read-success-getacl
  Conditions = [ """CEF:""", """ REST.GET.ACL """, """ dproc=endpoint-sqs """ ]
  ParserVersion = v1.0.0

aws-cloudtrail-cef = {
    Vendor = "Amazon"
    Product = "Amazon S3"
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Fields = [
      """cs6=\s*(-|({owner_id}[^\s]+))\s+(-|({bucket_name}[^\s]+))\s+\[?({time}\d\d\/\w{3}\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d\d\d\d)\]?\s+(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+(-|(arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?)|({assumed_role_arn}arn:aws:sts::\d+:assumed-role\/[^\s]+)\\?|({additional_info}[^\s]+))\s+(-|({request_id}[^\s]+))\s+({operation}[^\s]+)\s+(-|({key_name}[^\s]+))\s+"(-|({uri}[^"]+))"\s+(-|({http_response_code}\d+))\s+(-|({failure_code}({error_code}[^\s]+)))\s+(-|({bytes_out}\d+))\s+(\S+\s+){3}"(-|({referrer}[^"]+))"\s+"(-|({user_agent}[^"]+))"\s+(\S+\s+){3}(-|({cipher}[^\s]+))\s+(-|({auth_method}[^\s]+))\s+(-|({src_host}[\w.-]+))\s+(-|({tls}[^\s]+))\s+"""
    
}
```