Modification of the Swarm library to support structured outputs.

Original library: https://github.com/openai/swarm

**Modifications**

Added support for structured outputs using completions.parse()

Modified Agent class:

## `Agent` Fields

| Field            | Type                     | Description                                                                   | Default                      |
| ---------------- | ------------------------ | ----------------------------------------------------------------------------- | ---------------------------- |
| **name**         | `str`                    | The name of the agent.                                                        | `"Agent"`                    |
| **model**        | `str`                    | The model to be used by the agent.                                            | `"gpt-4o"`                   |
| **instructions** | `str` or `func() -> str` | Instructions for the agent, can be a string or a callable returning a string. | `"You are a helpful agent."` |
| **functions**    | `List`                   | A list of functions that the agent can call.                                  | `[]`                         |
| **tool_choice**  | `str`                    | The tool choice for the agent, if any.                                        | `None`                       |
| **response_format**  | `BaseModel` or `None`                   | Pydantic schema defining the response format for the agent | `None`                       |


## Install

Requires Python 3.10+


```shell
pip install git+https://github.com/mdavudov/sky_swarm_structured_output.git
```

