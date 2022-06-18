---
title: /club/create
position_number: 3.1
type: post
description: Create a club
parameters:
  - name: name
    content: The full name of the club. <strong>Required</strong>
  - name: description
    content: In 150 characters or fewer, what the club is about. <strong>Required</strong>
  - name: instagram
    content: The instagram username of the club
  - name: google_classroom_code
    content: The google classroom code of the club
  - name: signup_link
    content: A link to the club's signup form
  - name: clubfest_link
    content: A link to the club's clubfest video
content_markdown: |-
  The Club will be created in the database and the club object will be returned.
  {: .success }
left_code_blocks:
  - code_block: |-
      import axios from 'axios';
      const fetchData = async () => {
        const response = await axios.post({
          method: 'post',
          url: 'localhost:8000/api/v0/clubs/club/create',
          data: {
            name: "",
            description: "",
            clubfest_link: "",
            instagram: "",
            google_classroom_code: "",
            signup_link: "",
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
        "message": "Missing required field: Name",
      }
      ...
      {
        "status": "error",
        "message": "Character limit exceeded",
      }
      ...
      {
        "status": "error",
        "message": "Missing required field: Description",
      }
      ...
      {
        "status": "error",
        "message": "Resource Conflict: Name is taken already",
      }
    title: Error
    language: json
---
