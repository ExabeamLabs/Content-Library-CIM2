#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-network-app-fortigate
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """ logver=""", """ deviceExternalId=""", """ cat=""" ]
 
fortinet-fortigate-cef-network-traffic-info}{
   Name = fortinet-fortigate-kv-network-app-fortigate
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """ logver=""", """ deviceExternalId=""", """ cat=""" ]
 }

${IbmLotusNotesTemplates.ibm-lotus-notes}{
  Name = ibm-hclnotes-str-file-upload-success-pushing
  ParserVersion = "v1.0.0"
  Conditions = ["""  Pushing """, """ to """]
  Fields = ${IbmLotusNotesTemplates.ibm-lotus-notes.Fields}[
# system_info is removed
    """Pushing\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({src_file_name}[^"]+(\.({src_file_ext}[^\.\"]+)))))\"*"""
  ]
  DupFields = ["src_file_name -> file_name","src_file_ext -> file_ext"
}
```