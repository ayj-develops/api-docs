---
title: /club/slug/:slug/executives/add
position_number: 3.3
type: put
description: Adds an executive to the execs array in club object
parameters:
  - name: executive
    content: The id of the executive to be added <Strong>Required</Strong>
content_markdown:
left_code_blocks:
  - code_block: |-
      import axios from 'axios';
      const fetchData = async () => {
        const response = await axios.put({
          method: 'put',
          url: 'localhost:8000/api/v0/clubs/club/slug/:slug/executives/add',
          data: {
            executive: "new exec id"
          }
          headers: {Authorization: `Bearer ${your-token-here}`}
        });
        return response.data
      }
    title: React
    language: javascript
right_code_blocks:
  - code_block: |-
      {
        "name": "",
        "slug": "",
        "description": "",
        "execs": [
          "new exec id"
        ],
        "teachers": [],
        "clubfest_link": "",
        "socials": {
            "instagram": "",
            "google_classroom_code": "",
            "signup_link": ""
        },
        "events": 0,
        "posts": 0,
        "_id": "62ae471f503d631f2feaf6f9",
        "__v": 0
      }
    title: Response
    language: json
  - code_block: |-
      {
        "status": "error",
        "message": "Bad Request",
        "stacktrace": "stack trace here",
      }
      ...
      {
        "status": "error",
        "message": "Not found: :slug",
      }
    title: Error
    language: json
---
