---
title: Authentication
position_number: 2
parameters:
  - name:
    content:
content_markdown: |-
  You need to be authenticated for all API requests. To be authenticated means the client must have a valid Firebase credential access token that will be checked by middleware in the server before allowing the request to hit.

  Nothing will work unless you include the `Authorization: Bearer <token>` in the header.
  {: .error}
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
       import axios from 'Axios'

       const fetchData = async () => {
        const response = await axios.get('localhost:8000/api/v0/protected-endpoint', 
          headers: {
            Authorization: `Bearer ${your-token-here}`
          }
        );
        return response.data
       }
    title: Javascript
    language: javascript
---