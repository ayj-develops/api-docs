---
title: Errors
position_number: 3
parameters:
  - name:
    content:
content_markdown: |-

  Here are the status codes returned with the Error.

  | Code | Name         | Description                                               |
  | ---- | ------------ | --------------------------------------------------------- |
  | 200  | OK           | Success                                                   |
  | 201  | Created      | Creation Successful                                       |
  | 400  | Bad Request  | We could not process that action                          |
  | 401  | Unauthorized | We could not verify who you say you are                   |
  | 403  | Forbidden    | You do not have enough permission to access this resource |
  | 409  | Conflict     | There might be a resource with the same attributes        |

  All errors will return JSON in the following format.

  Stack trace might not be sent when the message is of sufficient detail or when it is treated as a custom validation error.

left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      {
        "status": "error",
        "message": "error message here",
        "stacktrace": "stack trace here",
      }
    title: Response
    language: json
---