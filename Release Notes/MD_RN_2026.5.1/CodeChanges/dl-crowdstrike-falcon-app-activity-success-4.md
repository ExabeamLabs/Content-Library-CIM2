# Code Changes for dl-crowdstrike-falcon-app-activity-success-4 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'crowdstrike-falcon-json-process-create-success-deliverlocalfxtocloud', 'crowdstrike-falcon-json-process-create-success-installedapplication', 'crowdstrike-falcon-json-process-create-success-agentconnect', 'crowdstrike-falcon-json-process-create-success-configstateupdate', 'crowdstrike-falcon-json-process-create-success-currentsystemtags','crowdstrike-falcon-json-app-activity-scriptcontrolscaninfo') && !InList(toLower(os), 'mac', 'lin', 'linux', 'win') |