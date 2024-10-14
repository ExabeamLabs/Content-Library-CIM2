#### Parser Content
```Java
{
Name = "microsoft-mssql-kv-database-delete-success-dl"
  Conditions = [ """.sql.class_type=""", """.sql.statement=""", """.sql.database_name""", """.sql.action_id="DL""" ]
  ParserVersion = "v1.0.0"

s-mssql-database-query-1 = {
      Vendor = Microsoft
      Product = MSSQL
      TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
      Fields = [
        """sql.server_instance_name=({host}[\w.-]+)""",
        """\.sql\.action_id="+({db_operation}\w+)\s*"""",
        """\.sql\.event_time="+({time}\d{4}-\d{2}-\d{2} (\d{2}:){2}\d{2}\.\d{7})"+""",
        """\.server_principal_name="*(({domain}[^\\]+?)[\\]{1,2})?({db_user}[^\s]+?)"*(\s+\.sql\.)""",
        """\.sql\.database_name=({db_name}[^=]+?)\s+\.sql""",
        """\.sql\.schema_name=({db_schema}[^=]+?)\s+\.sql""",
        """\.sql\.object_name=({db_object}[^=]+?)\s+\.sql\.\w+=""",
        """sql\.statement="+({db_query}[^"]+)"+\s+.sql"""
      ]
      DupFields = [ "db_user->user" ]
    },

  cef-sysmon-file-write = {
    Vendor = Microsoft
    Product = Sysmon
    TimeFormat = "epoch"
    Fields = [
      """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
      """({host}\S+) CEF:""",
      """\Wdvc=({host}[A-Fa-f:\d]+)""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """\Wrt=({time}\d{13})""",
      """\WeventId=({event_code}\d+)""",
      """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)""",
      """\Wdproc=({file_path}({file_dir}.*?)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s+(\w+=|$)""",
      """\Wdproc=({process_path}({process_dir}.*?)({process_name}[^\\]+?))\s+(\w+=|$)""",
      """\Wfname=.+?USERS\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """\Wfname=({file_path}({file_dir}.*?)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s+(\w+=|$)""",
      """\Wcs6=\{({process_guid}[^\}]+)""",
      """\Wdpid=({process_id}\d+)""",
      """\Wcs1=({object}.+?)\s+(\w+=|$)""",
    ]
    DupFields = [ "host->dest_host" 
}
```