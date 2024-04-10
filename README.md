# Latest workflow runs

This gets the result of latest runs of the given workflow.

This takes below parameters
- **-o | --org**: Required. GitHub Organization name
- **-w | --workflow**: Required. Workflow name. Provide the workflow file name (Ex: *code-ql.yml*)
- **-f | --outfile**: Optional. Output csv file name (Ex: *code-ql-runs.csv*), If not provided, it generates output file as *output.csv*
- **--verbose**: Optional. The flag to run the script in debug mode

This creates output
## How to run

Set the environment variable *GH_TOKEN* with your github token. This should have read access to workflows and its runs.
```
    export GH_TOKEN=$GITHUB_TOKEN
```
Execute the script

```
    python get-latest-workflow-runs.py --org $ORG_NAME --workflow $WORKFLOW_FILE_NAME
```

Examples:
```
    python get-latest-workflow-runs.py --org my-org --workflow code-ql.yml
```
To run with debug mode
```
    python get-latest-workflow-runs.py --org my-org --workflow code-ql.yml --verbose
```

