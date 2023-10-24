#### Parser Content
```Java
{
Name = "ibm-hclnotes-str-app-logout-closedsession"
  ParserVersion = "v1.0.0"
  Conditions = ["""  Closed session for """, """Databases accessed:""", """Documents read:""", """Documents written:""", """Transactions:"""]
  Fields = ${IbmLotusNotesTemplates.ibm-lotus-notes.Fields}[
# system_info is removed
  ]

ibm-lotus-notes = {
    Vendor = "IBM"
    Product = "HCL Notes"
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Fields = [
      """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))""",
      """from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({src_file_name}[^"]+(\.({src_file_ext}[^\.\"]+)))))\"*"""
    
}
```