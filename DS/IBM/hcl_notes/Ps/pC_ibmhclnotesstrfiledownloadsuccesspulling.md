#### Parser Content
```Java
{
Name = ibm-hclnotes-str-file-download-success-pulling
  ParserVersion = "v1.0.0"
  Conditions = ["""  Pulling """, """ from """]
  Fields = ${IbmLotusNotesTemplates.ibm-lotus-notes.Fields}[
# system_info is removed
  ]
  DupFields = ["src_file_name -> file_name","src_file_ext -> file_ext"]

ibm-lotus-notes = {
    Vendor = "IBM"
    Product = "HCL Notes"
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Fields = [
      """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
      """from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({src_file_name}[^"]+(\.({src_file_ext}[^\.\"]+)))))\"*"""
    
}
```