# Code Changes for crowdstrike-falcon-file-delete-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'crowdstrike-falcon-json-file-delete-success-deleted', 'crowdstrike-falcon-json-file-delete-success-executabledeleted') and InList(toLower(event_code), 'executabledeleted','filedeleted','processselfdeleted','volumesnapshotdeleted','wfpfiltertamperingfilterdeleted') && containsAny(toLower(os), 'mac') |