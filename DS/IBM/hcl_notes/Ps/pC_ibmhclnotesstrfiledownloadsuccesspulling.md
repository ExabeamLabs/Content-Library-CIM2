#### Parser Content
```Java
{
Name = ibm-hclnotes-str-file-download-success-pulling
  ParserVersion = "v1.0.0"
  Conditions = ["""  Pulling """, """ from """]

ibm-lotus-notes = {
    Vendor = "IBM"
    Product = "HCL Notes"
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Fields = [
      """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
      """from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*"""
    ibm-lotus-notes = {
    Vendor = "IBM"
    Product = "HCL Notes"
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Fields = [
      """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
      """from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*"""
    ]
  }
}
```