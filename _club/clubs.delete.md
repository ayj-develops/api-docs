---
title: /club/slug/:slug/delete
position_number: 3.2
type: delete
description: Delete a specific club by their slug
content_markdown: |-
  Finds the club by the slug, if not found the request is rejected.
  {: .warning}

  Deletes the club if found, and returns the deleted club object.
  {: .success}
left_code_blocks: 
  - code_block: |-
      import axios from 'axios';
      const fetchData = async () => {
        const response = await axios.post({
          method: 'delete',
          url: 'localhost:8000/api/v0/clubs/club/slug/:slug/delete',
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
        "execs": [],
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
