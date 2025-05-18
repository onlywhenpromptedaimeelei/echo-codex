# Codex Interaction Protocol

## Core Commands

- `INITIATE {system_name}`: Starts a system or service.
- `PROCESS {task_name} USING {data_block}`: Executes a task with given parameters.
- `QUERY {system_name} FOR {info}`: Retrieves information.
- `UPDATE {parameter} TO {value}`: Modifies system configuration.
- `TRAIN {model} WITH {dataset}`: Begins training on a specified dataset.
- `EVALUATE {model} ON {test_data}`: Evaluates model performance.
- `TUNE {model} WITH {params}`: Adjusts learning parameters.
- `SCHEDULE {task} AT {time}`: Schedules a timed task.
- `TERMINATE {process}`: Stops a running process.

## Response Format

- Success:
```json
{ "status": "success", "output": "result" }
```

- Error:
```json
{ "status": "error", "code": 400, "message": "description of the issue" }
```

## Example:
```bash
> PROCESS GenerateReport USING {dataset: "Q3_sales"}
< { "status": "success", "output": "Report generated" }
```
