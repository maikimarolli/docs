---
title: Stara Credentials
description: Credentials - Stara
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import useBaseUrl from '@docusaurus/useBaseUrl';

[1]: #get-the-stara-credentials
[2]: #create-a-stara-credentials
[3]: #delete-stara-credentials
[4]: /docs/docs/field_boundaries_overview
[5]: /docs/docs/beta_machines_endpoints

:::caution Services availability
This integration is under construction. For now, no data is being integrated yet.
:::

Form of a Stara Credentials resource:

```json
{
  "status": "str",
  "apiKey": "str",
  "accessToken": "str",
  "accessTokenClient": "str",
  "refreshToken": "str"
}
```

**Endpoints**

Description | Endpoints
--- | ---
[Get the Stara credentials][1] | <span class="badge badge--success">GET</span> `/users/{leafUserId}/stara-credentials`
[Create a Stara credentials][2] | <span class="badge badge--warning">POST</span> `/users/{leafUserId}/stara-credentials`
[Delete Stara credentials][3] | <span class="badge badge--danger">DELETE</span> `/users/{leafUserId}/stara-credentials`


## Stara Credentials Endpoints

### Get the Stara credentials
&nbsp<span class="badge badge--success">GET</span> `/users/{leafUserId}/stara-credentials`  

Get the Stara credentials of the Leaf User based on its `id` and returns a JSON with the credentials.

#### Request examples
<Tabs
defaultValue="sh"
values={[
  { label: 'cURL', value: 'sh', },
  { label: 'Python', value: 'py', },
  { label: 'JavaScript', value: 'js', },
]
}>
<TabItem value="js">

  ```js
  const axios = require('axios')
  const TOKEN = 'YOUR_TOKEN'

  const endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  const headers = { 'Authorization': `Bearer ${TOKEN}` }

  axios.get(endpoint, { headers })
      .then(res => console.log(res.data))
      .catch(console.error)
  ```

  </TabItem>
  <TabItem value="py">

  ```py
  import requests

  TOKEN = 'YOUR_TOKEN'

  endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  headers = {'Authorization': f'Bearer {TOKEN}'}

  response = requests.get(endpoint, headers=headers)
  print(response.json())
  ```

  </TabItem>
  <TabItem value="sh">

  ```shell
  curl -X GET \
      -H 'Authorization: Bearer YOUR_TOKEN' \
      'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  ```

  </TabItem>
</Tabs>

#### Response
A Stara credentials resource as a JSON.


### Create a Stara credentials 
&nbsp<span class="badge badge--warning">POST</span> `/users/{leafUserId}/stara-credentials`  
Create a Stara credential for the Leaf User.

#### Request examples
A Stara credential.

```json
{
  "apiKey": "str",
  "accessToken": "str",
  "accessTokenClient": "str",
  "refreshToken": "str"
}
```

<Tabs
defaultValue="sh"
values={[
  { label: 'cURL', value: 'sh', },
  { label: 'Python', value: 'py', },
  { label: 'JavaScript', value: 'js', },
  
  
]
}>
<TabItem value="js">

  ```js
  const axios = require('axios')
  const TOKEN = 'YOUR_TOKEN'

  const endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  const headers = { 'Authorization': `Bearer ${TOKEN}` }

  const data = {
    "apiKey": "str",
    "accessToken": "str",
    "accessTokenClient": "str",
    "refreshToken": "str"
  }

  axios.post(endpoint, data, { headers })
      .then(res => console.log(res.data))
      .catch(console.error)
  ```

  </TabItem>
  <TabItem value="py">

  ```py
  import requests

  TOKEN = 'YOUR_TOKEN'

  endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  headers = {'Authorization': f'Bearer {TOKEN}'}

  data = {
    "apiKey": "str",
    "accessToken": "str",
    "accessTokenClient": "str",
    "refreshToken": "str"
   }

  response = requests.post(endpoint, headers=headers, json=data)
  print(response.json())
  ```

  </TabItem>
  <TabItem value="sh">

  ```shell
  curl -X POST \
      -H 'Authorization: Bearer YOUR_TOKEN' \
      -H 'Content-Type: application/json' \
      -d '{"apiKey": "str", "accessToken": "str", "accessTokenClient": "str", "refreshToken": "str"}' \
      'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  ```

  </TabItem>
</Tabs>

#### Response
A Stara Credentials with status.



### Delete Stara credentials
&nbsp<span class="badge badge--danger">DELETE</span> `/users/{leafUserId}/stara-credentials`  
Delete Leaf User's Stara credentials.

#### Request examples
<Tabs
defaultValue="sh"
values={[
  { label: 'cURL', value: 'sh', },
  { label: 'Python', value: 'py', },
  { label: 'JavaScript', value: 'js', },
  
  
]
}>
<TabItem value="js">

  ```js
  const axios = require('axios')
  const TOKEN = 'YOUR_TOKEN'

  const endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  const headers = { 'Authorization': `Bearer ${TOKEN}` }

  axios.delete(endpoint, { headers })
      .then(res => console.log(res.data))
      .catch(console.error)
  ```

  </TabItem>
  <TabItem value="py">

  ```py
  import requests

  TOKEN = 'YOUR_TOKEN'

  endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  headers = {'Authorization': f'Bearer {TOKEN}'}

  response = requests.delete(endpoint, headers=headers)
  print(response.json())
  ```

  </TabItem>
  <TabItem value="sh">

  ```shell
  curl -X DELETE \
      -H 'Authorization: Bearer YOUR_TOKEN' \
      'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/stara-credentials'
  ```

  </TabItem>
</Tabs>