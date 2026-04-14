# Code Changes for vormetric-v-alert-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'vormetric-v-kv-file-read-success-code') && InList(toLower(access),'read_file', 'read_dir','create_file', 'make_dir','write_append', 'write_app') && InList(toLower(action), 'denied') |