#### Parser Content
```Java
{
Name = microsoft-o365-csv-file-success-sharepoint
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ ""","SharePoint","20""" ]
  Fields = [
    ""","({app}SharePoint)","\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z"(,("[^"]*"|[^,]*)){2},"[^"]*?({email_address}[^@]+@({email_domain}[^"\|]+))"(,[^,]*){10},"({access}({operation}[^"]+))",(("[^"]*"|[^,]*),){3}"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)",(("[^"]*"|[^,]*),){7}(|"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"),.*?,"SharePoint",(("[^"]*"|[^,]*),){10}(|"({share_path}[^"]+)"),(|"({file_name}[^"]+?(\.({file_ext}\w+))?)"),(|"({file_dir}[^"]+)"),""",
  ]
  ParserVersion = v1.0.0


}
```